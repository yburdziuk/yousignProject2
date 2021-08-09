# Technical test for YOUSIGN entreprise
II. Tech task Postman
Positive and negative test cases are present
Different types of execution (CSV data file available apart or random variables inserted direclty into the pre-request script)
The needed environement and variables are uploaded with project
Test 1 : Get users (GET method)

Return all users available

Test 2 : Positive Create a user using random variable (POST method)

Using the variables in the body part to create data for this test

Test 3 : Negative Create a user without the email (POST method)

Negative passing test case with the check of the status and the error message raised

Test 4 : Get the users created in step 2 (GET method)

Retrieve and check the user created in the test 2

Additional test : Positive Create a user using CSV data file Create the users by using the CSV data file (see the file in the project)

To execute with Newman :

newman run Yousign.postman_collection.json -e Yousign.postman_environment.json -d usersYousign.csv