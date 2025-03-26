Calculator Microservice

Overview

This microservice provides basic calculator functionalities via a REST API, including addition, subtraction, multiplication, and division operations. It is built using Node.js and Express.js, with Winston used for logging requests and responses.

Features

Supports four arithmetic operations: addition, subtraction, multiplication, and division.

Logs all incoming requests with details such as operation type, input values, and request method.

Error handling for invalid inputs and division by zero.

Logging implemented using the Winston library.

Prerequisites

Ensure you have the following installed before proceeding:

Node.js (version 14 or later)

npm (Node Package Manager)

API Endpoints

Each endpoint accepts two query parameters: num1 and num2.

Operation

Endpoint

Example Request

Addition

/add

/add?num1=5&num2=3

Subtraction

/subtract

/subtract?num1=5&num2=3

Multiplication

/multiply

/multiply?num1=5&num2=3

Division

/divide

/divide?num1=5&num2=3

Logging

Winston logs request details and errors.

Logs are stored in logs/combined.log and logs/error.log.

View logs in real-time using:

tail -f logs/combined.log

Error Handling

If num1 or num2 is not a valid number, the response will include an error message.

Division by zero is handled with a proper error response.

Invalid endpoints return a 404 error.
