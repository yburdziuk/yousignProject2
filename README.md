# Technical test for YOUSIGN entreprise

## II. Tech task Postman

* Positive and negative test cases are present
* Different types of execution (CSV data file available apart or random variables inserted direclty into the pre-request script)

<img width="519" alt="Capture d’écran 2021-08-09 à 17 07 44" src="https://user-images.githubusercontent.com/61992820/128729087-6ab26eab-f341-4f68-a0f2-17623f569bc0.png">
<img width="749" alt="Capture d’écran 2021-08-09 à 17 11 04" src="https://user-images.githubusercontent.com/61992820/128729589-9867232a-14e1-4c8c-862e-230af04b7f93.png">

CSV file must be uploaded while test execution 

Don't hesitate to change it as you want 

<img width="464" alt="Capture d’écran 2021-08-09 à 17 08 33" src="https://user-images.githubusercontent.com/61992820/128729463-50b445d7-e334-40f9-960e-6ff293c9cf6a.png">

* The needed environement and variables are uploaded with project

-> Environement & variables: Yousign.postman_environment.json

-> CSV data file : usersYousign.csv

**Test 1 : Get users (GET method)**

Return all users available

**Test 2 : Positive Create a user using random variable (POST method)**

Using the variables in the body part to create data for this test

**Test 3 : Negative Create a user without the email (POST method)**

Negative passing test case with the check of the status and the error message raised

**Test 4 : Get the users created in step 2 (GET method)**

Retrieve and check the user created in the test 2

**Additional test : Positive Create a user using CSV data file**

Create the users by using the CSV data file (see the file in the project)

## To execute with Newman and make a report using the reporter [newman-reporter-htmlextra](https://github.com/DannyDainton/newman-reporter-htmlextra): ##
⚠️ Don't forget to indicate the CSV file, otherwise the test which is based on it will fail ⚠️

**newman run Yousign.postman_collection.json -e Yousign.postman_environment.json -r htmlextra --reporter-htmlextra-export ./results/report.html**

⚠️ Make sure to specify the path where the output HTML file will be stocked ⚠️

(like here : *-r htmlextra --reporter-htmlextra-export ./results/report.html*)
