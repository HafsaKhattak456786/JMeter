# Assignment No. 5 – API Testing with JMeter (Books API)

## Project Overview
This project demonstrates API testing using Apache JMeter on the Simple Books API.
The objective is to design and execute API test plans covering CRUD operations
and CSV-based data-driven testing.

Due to API limitations, the Books endpoint is read-only. Therefore, full CRUD
operations have been implemented using the Orders API.

## Learning Objectives
- Build JMeter test plans using Thread Groups, Samplers, and Listeners
- Automate CRUD API workflows
- Implement CSV-based data-driven testing in JMeter
- Validate API responses using assertions

## Tools & Technologies
- Apache JMeter
- Simple Books API

## APIs Covered
### Books API (Read-Only)
- GET /books
- GET /books/{id}

### Orders API (CRUD)
- POST /orders
- GET /orders/{orderId}
- PATCH /orders/{orderId}
- DELETE /orders/{orderId}
- GET /orders/{orderId} (after delete for validation)

## Test Workflow
1. Create an order using POST request
2. Retrieve the created order using GET
3. Update the order using PATCH
4. Delete the order using DELETE
5. Validate deletion using GET request

## Data-Driven Testing
CSV-based data-driven testing is implemented using a CSV Data Set Config.
Multiple POST requests are executed using data from the CSV file.

## Project Files
- Books_API_CRUD_TestPlan.jmx – JMeter test plan
- data.csv – CSV file for data-driven testing
- README.md – Project documentation

## How to Run the Project
1. Open Apache JMeter
2. Load the `Books_API_CRUD_TestPlan.jmx` file
3. Ensure `data.csv` is placed in the same directory
4. Run the test plan and view results using listeners

## Notes
- The Books API does not support POST, PUT, PATCH, or DELETE operations.
- CRUD operations are implemented using the Orders API as per API capabilities.
