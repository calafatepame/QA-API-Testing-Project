# API Findings – Users

## 1. Context

During the execution of test cases against the `/users` resource in JSONPlaceholder, differences were observed between the expected results and the actual API responses.

The following findings document the behavior observed during automated execution with Postman and Newman.

## 2. Identified Findings

### H-01 – Acceptance of requests without an email field

- **Related test case:** TC10
- **Method:** POST
- **Expected result:** HTTP 400 and request rejection.
- **Actual result:** HTTP 201 Created.
- **Observed behavior:** The API accepted the request without the email field and returned an ID.

### H-02 – Acceptance of an empty request body

- **Related test case:** TC11
- **Method:** POST
- **Expected result:** HTTP 400 and request rejection.
- **Actual result:** HTTP 201 Created.
- **Observed behavior:** The API accepted the request with an empty body and returned an ID.

### H-03 – Acceptance of a numeric email value

- **Related test case:** TC12
- **Method:** POST
- **Expected result:** The email field should be a string.
- **Actual result:** HTTP 201 Created.
- **Observed behavior:** The response preserved the numeric value sent in the email field.

### H-04 – Acceptance of an invalid email format

- **Related test case:** TC13
- **Method:** POST
- **Expected result:** Request rejection.
- **Actual result:** HTTP 201 Created.
- **Observed behavior:** The API accepted the request with an invalid email format.

### H-05 – Internal server error when sending malformed JSON

- **Related test case:** TC14
- **Method:** POST
- **Expected result:** HTTP 400 or 422.
- **Actual result:** HTTP 500 Internal Server Error.
- **Observed behavior:** The API returned an internal server error when receiving malformed JSON.

## 3. Analysis

The results show that, during execution, the API accepted several requests containing incomplete data or unexpected formats.

An HTTP 500 response was also observed when sending malformed JSON.

These results highlight differences between the validation expectations defined for this exercise and the behavior observed in the API.

## 4. Limitations

JSONPlaceholder is a public testing API. Therefore, these findings describe its observed behavior and do not necessarily represent defects in a production application.

The rejection expectations used in the test cases were defined for this QA exercise.

## 5. Evidence

Execution results can be found in:

- Postman collection: `collection/users-api-testing.postman_collection.json`
- Newman report: `reports/newman-report.html`
- Execution screenshots: `evidence/`
