# Postman API Testing

# Project Overview

This project demonstrates REST API functional testing using Postman and the GoREST API. It covers CRUD operations, request chaining, and response validation.

# Tools & Technologies

- Postman
- GoREST API
- Git
- GitHub

# Collection Structure

- **request chaining, dynamic data generation, response validations**: the CRUD workflow
- **negative testing**: invalid and missing data, duplicate data and authentication failure

# CRUD Scenarios

| HTTP Method | Operation | Description |
|---|---|---|
| POST | Create User | Create a new user |
| GET | Retrieve User | Retrieve the created user |
| PUT | Update User | Update user information |
| DELETE | Delete User | Delete the user |

**Request Workflow:** POST → GET → PUT → DELETE

The user ID generated during the POST request is stored and reused in subsequent requests.

# Negative Testing

| Scenario | Method | Expected Status | Validation |
|---|---|---|---|
| Empty name | POST | 422 | Field is `name`, message "can't be blank" |
| Invalid email | POST | 422 | Field is `email`, message "is invalid" |
| Empty gender | POST | 422 | Field is `gender` |
| Invalid gender | POST | 422 | Field is `gender` |
| Empty status | POST | 422 | Field is `status`, message "can't be blank" |
| Duplicate email | POST | 422 | Field is `email`, message "has already been taken" |
| Invalid token (no auth) | POST | 401 | Message "Authentication failed" |

# Testing Performed

- Validated HTTP methods, status codes and status text.
- Validated response headers (content-type).
- Verified response body fields, data types and values.
- Validated response time against a threshold.
- Validated the response against a JSON schema.
- Used collection variables for request chaining.
- Generated dynamic test data in pre-request scripts.
- Tested error handling with negative scenarios.


# Screenshot

<img width="1366" height="768" alt="Negative test results" src="https://github.com/user-attachments/assets/3fcb7583-c4a9-4e47-ad98-16841d875185" />

<img width="1366" height="768" alt="Negative test results" src="https://github.com/user-attachments/assets/e83d96ab-f3e1-4026-b2d5-b55a4113cf63" />

<img width="1366" height="768" alt="Collection run results" src="https://github.com/user-attachments/assets/3568aa4c-ab28-4f19-b35b-9fdad6637648" />

<img width="259" height="600" alt="Collection folders" src="https://github.com/user-attachments/assets/9a331ebb-ae1f-4d51-ac8a-fa00736fa357" />

# How to Run

1. Download or clone this repository.
2. Import the Postman collection into Postman.
3. Configure your GoREST Bearer Token.
4. Run individual requests or execute the collection using Collection Runner.


**Note**: Keep your personal access token private. Do not commit real API tokens to GitHub.

# Future Improvements
- API automation using Playwright.
- Automated test execution using GitHub Actions.
