# 🧪 Project #4 – RESTful Booker API Testing

This project demonstrates comprehensive end-to-end API testing using Postman for the [RESTful Booker API](https://restful-booker.herokuapp.com). The API simulates a hotel booking system and supports full CRUD operations. The collection includes positive and negative test cases, schema validation, dynamic data handling, and authentication scenarios.

---

## 📄 Project Overview

- **API Type:** RESTful
- **Base URL:** `https://restful-booker.herokuapp.com`
- **Purpose:** Simulate a complete booking lifecycle using chained requests with assertions
- **Focus Areas:** Create, Read, Update, Delete (CRUD), token authentication, schema validation, and dynamic data

---

## 🎯 Objectives

- Validate core booking functionalities (Create, Read, Update, Delete)
- Test authentication and token generation
- Perform schema validation using JSON Schema
- Automate test assertions using JavaScript
- Explore dynamic data generation and environment variables
- Simulate end-to-end booking lifecycle with real-time validation

---

## 🧰 Tools & Technologies

- 🧪 Postman (v10+)
- 📜 JavaScript (for test scripting)
- 📄 JSON Schema (for response validation)
- 🔐 Basic Auth & Token-based Auth
- 🌐 RESTful API principles
- 🧪 Dynamic Postman variables (e.g., `{{$randomLastName}}`, `{{$randomInt}}`)

---

## 📦 Collection Structure & Workflow

| Step | Request Name                                       | Method | Auth Required | Description                                      |
|------|----------------------------------------------------|--------|----------------|--------------------------------------------------|
| 1️⃣   | Create Booking TC (Positive)                      | POST   | ❌ No           | Test cases to create bookings                    |
| 2️⃣   | ❌ Create Booking Negative - No Headers           | POST   | ❌ No           | Invalid test without required headers            |
| 3️⃣   | HealthCheck API                                   | GET    | ❌ No           | Ping endpoint to verify API availability         |
| 4️⃣   | GetBookingIds (All, By Name, By Params)           | GET    | ❌ No           | Retrieve booking IDs using filters               |
| 5️⃣   | GetBooking by Single ID                           | GET    | ❌ No           | Fetch booking details by ID                      |
| 6️⃣   | 🔐 Full Update Booking by ID                      | PUT    | ✅ Yes          | Update entire booking record                     |
| 7️⃣   | 🔐 Partial Update Booking by ID                   | PATCH  | ✅ Yes          | Update specific fields in a booking              |
| 8️⃣   | 🔐 Delete Booking by ID                           | DELETE | ✅ Yes          | Delete a booking using ID                        |
| 9️⃣   | Create Token Request                              | POST   | ❌ No           | Generate token for authenticated requests        |
| 🔁    | End-to-End Sequence                               | Mixed  | ✅/❌ Mixed     | Create → Update → Retrieve (validate full flow)  |

---

## 🧪 Sample Test Assertions

- ✅ Status code is 200
- ✅ Response time < 200ms
- ✅ Response body contains expected booking fields
- ✅ JSON schema validation for booking structure
- ✅ Token and booking ID are not null
- ✅ Stored values reused between requests

---

## 🌐 Environment Setup

### 🔧 Environment File

Use `New Environment.postman_environment.json` with:

| Variable   | Description                          |
|------------|--------------------------------------|
| `url`      | Base API URL                         |
| `bookingId`| Stores the ID of the created booking |
| `token`    | Stores the authentication token      |

### 🌍 Global Variable

Set the following if not using environment:

| Variable | Value                                 |
|----------|----------------------------------------|
| `url`    | `https://restful-booker.herokuapp.com` |

---

## 🛠️ How to Use

1. Import the collection and the environment file into Postman.
2. Set or confirm the `url` variable is correct.
3. Run the "Create Token Request" to generate a token.
4. Execute the "Create Booking TC" to create a booking and store the ID.
5. Follow with update, fetch, or delete requests using the saved variables.
6. Monitor results in the Test Results tab or Postman console.

---

## ✅ Recommendations for Enhancement

- Add negative test cases for invalid payloads and unauthorized access
- Integrate with Newman for CLI-based testing
- Include CI/CD pipeline integration (e.g., GitHub Actions)
- Use schema validation on all major response objects
- Add visual API workflow documentation or diagrams

---

## 📄 License

This project is intended for educational and non-commercial use only.

---

## 👨‍💻 Author

**Chirag Rathava**  
Postman Student Expert Candidate  
📧 [rathavachirag921@gmail.com](mailto:rathavachirag921@gmail.com)

---

Happy Testing! 🚀
