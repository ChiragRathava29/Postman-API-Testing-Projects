# 🧪 Project #2 – SOAP API Testing: Number to Words

This project demonstrates how to test a SOAP-based web service using Postman. The service under test is the **Number Conversion API** provided by [DataAccess.com](https://www.dataaccess.com/webservicesserver/NumberConversion.wso), specifically the `NumberToWords` operation, which converts numeric input into its English word representation.

### 🎯 Objective

To validate the behavior of the `NumberToWords` SOAP operation under various input conditions, including:
- Valid positive numbers
- Missing headers
- Negative numbers
- String and alphanumeric inputs
- Decimal values

### 🧰 Tools & Technologies
- **Postman** – for sending SOAP requests and organizing test cases
- **SOAP/XML** – for request formatting
- **JavaScript** – for basic test scripting (console logs, future assertions)

### 📦 Collection Details
- **Collection Name:** Project #2 - SOAP
- **Schema Version:** v2.1.0
- **Base URL Variable:** `{{c_url}}` → `https://www.dataaccess.com`
- **Target Endpoint:** `/webservicesserver/NumberConversion.wso`
- **Authentication:** No authentication required

---

## 🧪 Test Cases

| Test Case | Description                        | Input     | Type       |
|-----------|------------------------------------|-----------|------------|
| TC#1      | Valid number input                 | `235`     | Positive   |
| TC#2      | Missing headers                    | `235`     | Negative   |
| TC#3      | Negative number                    | `-1`      | Negative   |
| TC#4      | String input                       | `"Chirag"`| Negative   |
| TC#5      | Decimal number                     | `0.5`     | Negative   |
| TC#6      | Alphanumeric input                 | `"Chirag"`| Negative   |

---

## 🛠️ How to Use

1. Import the collection into Postman.
2. Set the environment variable `c_url` to `https://www.dataaccess.com`.
3. Run each test case individually or as part of a collection runner.
4. Observe the responses and validate against expected behavior.

---

## ✅ Recommendations for Improvement

- Add test scripts to validate response status codes and body content.
- Include assertions for expected vs. actual results.
- Document expected SOAP responses for each test case.
- Use dynamic variables and chaining for more advanced testing.

---

## 📌 Notes

- This project is part of a learning initiative focused on SOAP API testing.
- It demonstrates both functional and negative testing approaches.
- Future enhancements may include automated validations and CI integration.

---

## 📄 License

This project is open for educational and non-commercial use.

---

🧠 Created with 💡 by Chirag Rathava