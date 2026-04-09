# API Testing Project – Users endpoint

## Description:

This project contains API tests executed using Postman for the public endpoint:

https://jsonplaceholder.typicode.com/users

The objective of this project is to practice API testing using functional and negative test scenarios and document bugs found during testing.



## Test scope:

The following validations were performed:

• Status code validation  
• Response time validation  
• JSON structure validation  
• Data type validation  
• Negative testing  
• Invalid input testing  
• Non-existing resources testing  



## Test cases included:

TC01 – Get all users  
TC02 – Get user by valid ID  
TC03 – Get non existing user  
TC04 – Invalid ID format  
TC05 – Boundary value (ID = 0)  
TC06 – Negative ID  
TC07 – Decimal ID  
TC08 – Empty ID  
TC09 – POST create user valid data  
TC10 – Invalid email format  
TC11 – Empty request body  
TC12 – Invalid data types  
TC13 - Invalid Email Format
TC14 - Invalid Email Format
TC15 - Invalid Email Format
TC16 - Invalid Email Format


## Tools used:

• Postman  
• Jira (bug reporting)  
• GitHub  
• JSONPlaceholder API  



## Test approach:

Tests were executed manually and basic automation was implemented using Postman test scripts.

Each request includes validations for:

• Status codes  
• Response structure  
• Required fields  
• Data types  



## Bugs found during testing:

BUG-01 – API accepts invalid email format  
BUG-02 – API accepts empty request body  
BUG-03 – API accepts invalid data types  
BUG-04 – Malformed JSON returns success instead of validation error  

Bugs were documented in Jira following standard bug reporting structure:
Summary, Steps, Expected Result, Actual Result and Evidence.



## Test design techniques used:

• Equivalence partitioning  
• Boundary value analysis  
• Negative testing  



## What I learned:

• How to test APIs using Postman  
• How to create automated checks in Postman  
• How to design test cases  
• How to report bugs in Jira  
• How to identify negative scenarios  
• Importance of validation in APIs  



## Observations:

The API returns the same response for:

• Invalid ID format  
• Non existing ID  

This could make error differentiation difficult in real applications.



## Author:

QA practice project created as part of my API Testing learning process.
