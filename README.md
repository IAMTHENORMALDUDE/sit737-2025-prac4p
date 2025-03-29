# SIT737-2025-Prac4P: Calculator Microservice

## Overview

This project implements a simple calculator microservice using Node.js and Express. It provides REST API endpoints for basic arithmetic operations (addition, subtraction, multiplication, division) and includes logging using Winston.

## Setup Instructions

1. **Prerequisites**:

   - Node.js installed
   - Git installed
   - Visual Studio Code (optional)

2. **Clone the Repository**:

   ```bash
   git clone https://github.com/IAMTHENORMALDUDE/sit737-2025-prac4p.git
   cd sit737-2025-prac4p
   ```

3. **Install Dependencies**:

   ```bash
   npm install
   ```

4. **Run the Application**:

   ```bash
   node index.js
   ```

5. **Test the Endpoints**:

   - Addition: `GET http://localhost:3000/add?num1=5&num2=3`
   - Subtraction: `GET http://localhost:3000/subtract?num1=5&num2=3`
   - Multiplication: `GET http://localhost:3000/multiply?num1=5&num2=3`
   - Division: `GET http://localhost:3000/divide?num1=6&num2=2`

6. **View Logs**:
   ```bash
   tail -f logs/combined.log
   ```

## API Endpoints

- `/add`: Adds two numbers
- `/subtract`: Subtracts num2 from num1
- `/multiply`: Multiplies two numbers
- `/divide`: Divides num1 by num2 (returns error if num2 is 0)

## Error Handling

- Invalid numbers: Returns 400 with `{ "error": "Invalid input: Both parameters must be numbers" }`
- Division by zero: Returns 400 with `{ "error": "Division by zero is not allowed" }`

## Logging

- Uses Winston to log requests and results to console, `logs/error.log`, and `logs/combined.log`.
