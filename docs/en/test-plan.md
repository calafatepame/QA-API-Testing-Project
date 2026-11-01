# Test Plan – Users API

## 1. General Information

| Field | Description |
|---|---|
| Project | QA API Testing Project |
| API under test | JSONPlaceholder |
| Resource | Users |
| Main endpoint | `https://jsonplaceholder.typicode.com/users` |
| HTTP methods | GET and POST |
| Tools | Postman, Newman and GitHub Actions |
| Testing types | Functional, positive, negative and response validation testing |

## 2. Objective

To verify the behavior of the Users resource in the JSONPlaceholder API by performing functional tests on the GET and POST methods.

The tests aim to validate HTTP status codes, response structure and data types, required fields, and response times.

The project also aims to automate test execution using Postman and Newman and integrate it into a CI/CD workflow with GitHub Actions.

## 3. Scope

### In Scope

- Retrieve the list of users using GET.
- Retrieve users by ID.
- Send requests with non-existent IDs or invalid ID formats.
- Create users using POST.
- Send requests with incomplete, empty, or unexpected data formats and types.
- Validate HTTP status codes.
- Verify response structure, properties and data types.
- Check response times.
- Automate test execution.

### Out of Scope

- Authentication and authorization testing.
- Load and advanced performance testing.
- Security testing.
- Actual persistence of created users.
- User interface testing.

## 4. Test Strategy

The following testing techniques were applied:

- **Functional testing:** verification of endpoint behavior.
- **Positive testing:** requests with valid data.
- **Negative testing:** requests with invalid, incomplete or unexpected IDs and data.
- **Response validation:** verification of HTTP status codes, JSON structure, properties and data types.
- **Boundary analysis:** exploration of values such as zero, negative and decimal IDs.
- **Automated testing:** execution of assertions through Postman scripts and Newman.

## 5. Test Environment and Tools

| Element | Description |
|---|---|
| API | JSONPlaceholder |
| Environment | Public testing API |
| HTTP client | Postman |
| Test runner | Newman |
| Automation | GitHub Actions |
| Data format | JSON |
| Protocol | HTTP/HTTPS |

## 6. Entry Criteria

- API endpoint availability.
- Configured Postman collection.
- Defined test cases.
- Newman installed and operational for local execution.

## 7. Exit Criteria

- Execution of the defined test cases.
- Recording of test results.
- Identification and documentation of differences between expected and actual results.
- Availability of execution evidence.

Results are documented regardless of whether assertions pass or fail.

## 8. Execution Results

The collection contains 16 automated requests executed through Newman.

The analyzed execution produced the following results:

- 58 assertions executed.
- 48 assertions passed.
- 10 assertions failed.
- 16 requests executed without request-level errors.

The differences identified are documented in the API findings file.

## 9. Considerations

JSONPlaceholder is a public testing API. The results describe the behavior observed during test execution and should not automatically be interpreted as defects in a production system.

The validation expectations used in the tests represent the criteria defined for this QA exercise.
