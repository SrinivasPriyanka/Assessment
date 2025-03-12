# API Test Document 
## Overview
This repository contains an API test suite for validating various JSON responses from a REST API. The tests are written in Postman and ensure that each object in the API response contains the required properties (ID and Title), along with other checks as specified in the schema.
## Instructions on How to Import and Run the Tests
1. **Install Postman** :
   To run the tests, you need to have Postman installed on your system. If you don’t have it already, you can download and install it from the official website:
   - Download Postman - https://www.postman.com/downloads/
2. **Import the Postman Collection** :
   - **Download the Postman Collection** : The collection file **(“OpenChargeMapAPI.postman”)** which is available in this repository.
   - **Import the Collection** :
     - Open Postman.
     - Click on the Import button in the top-left corner.
     - Select the File tab and click Choose Files.
     - Select the OpenChargeMapAPI.postman file and click Open.
     - The collection will be imported into your Postman workspace.
3. **Necessary Setup Steps** :
   API Key:To get a valid api key visit the Web URL and inspect the API calls triggered. On the request headers of the API calls pointing to the above base url you will find a valid Api key to use for your requests. Set this key in the Postman Authorization.
4. **Run the Tests** :
   - **Select the Collection:** In the left sidebar, select the import collection.
   - **Run the Collection:**
     - Click the Run button at the top-right of Postman.
     - This will open the Collection Runner, where you can choose to run all the requests or select specific requests.
   - **View Results:**
     - After running the tests, Postman will display the results for each request (Pass/Fail).
     - You can inspect the response data and see detailed information about each test in the results section.
## Test Results and Observations 
  After running the tests, you will see the following results for each endpoint:
  - Pass: If the response meets the expected structure and contains the required properties ( Status code, Response time, Schema validation, ID and Title), the test will pass.
  - Fail: If any of the assertions fail (Status code, Response time, Schema validation, ID and Title), the test will fail, and you will be provided with details about which property was missing.
## Analysis of Test Results
  - Success: If all tests pass, it indicates that the API returns consistent and complete data across all objects in the response.
  - Failures: It may indicate that the API is returning incomplete or malformed data for some items.
## Limitations:
  - The tests currently only check for the existence of the Status code, Response Time, Validations on POI objects, ID, AddressInfo, NumberOfPoints. They do not check the correctness or validity of these values.
  - The tests assume that the API will always return consistent data types, If the API changes its structure or returns different data types, the tests may need to be updated accordingly.




    
     
