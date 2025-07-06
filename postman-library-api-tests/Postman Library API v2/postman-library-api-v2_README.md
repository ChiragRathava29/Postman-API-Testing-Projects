# 📚 Postman Library API v2 – API Testing

This project tests a fictional digital library system using Postman. It includes endpoints to manage books, along with a skill check integration to demonstrate scripting and variable usage.

## 🌐 Base URL  
🔗 `https://library-api.postmanlabs.com`

## 🔐 Authentication  
- **Type:** API Key  
- **Key:** `api-key`  
- **Value:** `postmanrulz`  
- **Applied At:** Collection Level

## 📌 Endpoints Covered

| Name              | Method | Endpoint                                  | Description                        |
|-------------------|--------|-------------------------------------------|------------------------------------|
| Get Books         | GET    | `/books`                                  | Retrieve all books                 |
| Get Fiction Books | GET    | `/books?genre=fiction&checkedOut=false`   | Filter fiction books               |
| Get Book by ID    | GET    | `/books/:id`                              | Retrieve a book by its ID          |
| Add Book          | POST   | `/books`                                  | Add a new book                     |
| Checkout Book     | PATCH  | `/books/:id`                              | Mark a book as checked out         |
| Delete Book       | DELETE | `/books/:id`                              | Delete a book                      |
| Skill Check       | POST   | `{{skillcheckBaseUrl}}?movieName=...`     | Submit actor name & store variable |

## 🧪 Test Scripts Used

- Extract and store the `id` of a newly created book
- Save `favoriteActor` from the skill check response
- Use of environment variables and pre-request scripts
