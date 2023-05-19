# Ultra API tech task solution
This repository contains Postman collection and environment which are solutions to Ultra api tech task. Solution scontains tests for (users which is one of four resources) available on  https://gorest.co.in/ web page.

## About the solution
I decided to create multiple variants of REST API requests to cover as many scenarios as possible. I have fouced on both positive and negative scenarios. The collection includes test for basic CRUD operations, to be specific for GET all, GET one, POST, PATCH and DELETE requests.

Tests are design to verify the functional flow:
- Create a new user
- Verify if user was created
- Update already created user
- Verify if user has been updated
- Delete a user
- Verify if user has been deleted properly

All the tests verifies:
- positive and negative scenarios
- responses headers
- if returned data has proper format
- if returned data has proper values
- request responses (set to 1000 for now)

## Instructions
To run tests locally follow the steps below:
1. Make sure to have Node installed (if not download it from nodejs site).
2. Create new folder and move there both: postman collection and environment files.
3. Open CLI and navigate to the folder created above.
4. Install newman `npm install -g newman`
5. Run collection `newman run ultra-api-tech-task.postman_collection.json -e ultra-api-tech-task-environment.postman_environment.json --env-var token={TOKEN}` but replace TOKEN variable with your generated token.

This solution is also included as a part of CI/CD configuration using GitHub Actions. The solution and results can be found here [link](https://github.com/LukaszKulyk/ultra-api-tech-tas/actions/workflows/ultra-api-tech-task.yml)
