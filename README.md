# Login REST API on AWS

A simple login system built on AWS. A web page sends the username and password to a REST API, which checks them and returns success or failure.

## Architecture
HTML page → API Gateway (POST /login) → Lambda → DynamoDB

## AWS services used
- API Gateway: exposes the /login REST endpoint
- Lambda: login validation logic
- DynamoDB: stores user records
- IAM: permissions for Lambda to read DynamoDB

## Files
- userslogin20.html: login page (front end)
- lambda_function.py: backend code

## How it works
1. User enters username and password
2. The page sends a POST request with JSON to the API
3. Lambda looks up the user in DynamoDB
4. API returns { "success": true/false }

## What I learned
Building and connecting API Gateway, Lambda and DynamoDB, and handling CORS and IAM permissions.
