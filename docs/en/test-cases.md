# Test Cases – Users API

## 1. General Information

The following test cases cover the `/users` resource in JSONPlaceholder and are organized by HTTP method: GET and POST.

The test cases were executed using a Postman collection and automated with Newman.

## 2. GET Test Cases

| ID | Scenario | Expected Result | Actual Result |
|---|---|---|---|
| TC01 | Retrieve the list of users | HTTP 200 and an array response | Passed |
| TC02 | Retrieve a user with a valid ID | HTTP 200 and user data | Passed |
| TC03 | Retrieve a non-existent user (ID 999) | HTTP 404 | Passed |
| TC04 | Retrieve a user using an alphabetical ID | HTTP 404 | Passed |
| TC05 | Retrieve a user with ID 0 | HTTP 404 | Passed |
| TC06 | Retrieve a user with a negative ID | HTTP 404 | Passed |
| TC07 | Retrieve a user with a decimal ID | HTTP 404 | Passed |
| TC08 | Send a request to the endpoint without an ID | HTTP 200 and a list of users | Passed |

## 3. POST Test Cases

| ID | Scenario | Expected Result | Actual Result |
|---|---|---|---|
| TC09 | Create a user with valid data | HTTP 201 and user data | Passed |
| TC10 | Create a user without an email field | HTTP 400 and request rejection | HTTP 201. The API accepted the request without an email |
| TC11 | Create a user with an empty body | HTTP 400 and request rejection | HTTP 201. The API accepted the request |
| TC12 | Send an email field with a numeric data type | The email field should be a string | HTTP 201. The response preserved the numeric value |
| TC13 | Send an email with an invalid format | Request rejection and no user creation | HTTP 201. The API accepted the request |
| TC14 | Send malformed JSON | HTTP 400 or 422 | HTTP 500 Internal Server Error |
| TC15 | Send empty required fields | The collection expects HTTP 201 and accepts an empty name | HTTP 201. The empty name was returned |
| TC16 | Send a long name | HTTP 201 and a response containing a string name | HTTP 201. The request was accepted |

## 4. Results and Considerations

- Results correspond to one execution of the collection against JSONPlaceholder.
- Cases TC10, TC11, TC12, TC13 and TC14 showed differences between expected and actual results.
- TC15 and TC16 verify data acceptance; they do not check whether the API rejects empty fields or long names.
- A failed assertion represents a difference between the behavior observed and the expectation defined in the test script.

## 5. Traceability

The test cases are implemented in the following collection:

`collection/users-api-testing.postman_collection.json`

Automated execution is performed using Newman.
