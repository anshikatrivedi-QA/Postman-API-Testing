# Postman API Testing

# Project Overview

This project demonstrates REST API functional testing using Postman and the GoREST API. It covers CRUD operations, request chaining, and response validation.

# Tools & Technologies

- Postman
- GoREST API
- Git
- GitHub

# API Testing Scenarios

The project covers the following CRUD operations:

| HTTP Method | Operation | Description |
|---|---|---|
| POST | Create User | Create a new user |
| GET | Retrieve User | Retrieve the created user |
| PUT | Update User | Update user information |
| DELETE | Delete User | Delete the user |

# Testing Performed

- Validated HTTP methods and API requests.
- Checked response status codes.
- Validated response headers and cookies.
- Verified response body fields and values.
- Used JavaScript and Postman assertions for response validation.
- Used collection variables to store and reuse user IDs.
- Implemented request chaining to execute CRUD operations in sequence.
- Used dynamic test data generation for user creation.

# Request Workflow

POST → GET → PUT → DELETE

The user ID generated during the POST request is stored and reused in subsequent requests.

# How to Run

1. Download or clone this repository.
2. Import the Postman collection into Postman.
3. Configure your GoREST Bearer Token.
4. Run individual requests or execute the collection using Collection Runner.

**Note**: Keep your personal access token private. Do not commit real API tokens to GitHub.

# Future Improvements
- API automation using Playwright.
- Automated test execution using GitHub Actions.
