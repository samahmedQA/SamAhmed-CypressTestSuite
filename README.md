# Cypress-Test-Framework
A robust end-to-end test automation framework using Cypress, integrated with CI/CD pipelines and the Sorry Cypress Dashboard for seamless reporting and execution.

---

## **Dashboard and Results**

![image](https://github.com/user-attachments/assets/77f6f442-c6a6-4e73-b15b-a8717ee9961d)

### **Sample Test Results:**
![Test Results](https://github.com/user-attachments/assets/fb10d0f3-d056-4bda-a6a6-a6dd412131a2)

---

## **Installation**

### **Prerequisites:**
- [Node.js 18.16.0 LTS](https://nodejs.org/en/download/)
- [Visual Studio Code](https://code.visualstudio.com/)

### **Steps to Install:**
1. Clone the repository:
   ```bash
   git clone https://github.com/samahmedQA/SamAhmed-CypressTestSuite.git
   cd SamAhmed-CypressTestSuite


Install Dependencies
Run the following command to install all project dependencies:
npm install


---

## **Write Code**

To add new test cases, follow these steps:

### ** Create a New Spec File**
1. Name your file using the format:
TC00*_SampleTest*_spec.js         Example: TC001_Login_Spec.js.
2. Add Test Logic
Use the PageObjects/ directory for reusable methods like login.
Place helper methods in support/actions.js for common utilities.
3. Use Test Data
Store reusable test data in the data/testdata.js file.
4. Mock Data (if needed)
Add mock data files to the fixtures/ folder for scenarios requiring mocked inputs.

#### Configure/update/set Test Environments:

- Open config and update test environment urls,user,pass and update it to config.js
- Test environment json files names are case sensitive
- To run test on specific environment update `configFile=uat or configFile=prod`


#### Setup SorryCypress Dashboard:
- `docker-compose up -d`

#### Test:

- `test:cypress` run tests in sorry cypress dashboard
- `npm run cy:chrome` run tests in chrome browser
- `npm run cypress:open` for test development and run(_Test Watcher is set to false_)
- `npm run cy:test` run all tests in headless
- `npx cypress run --env configFile=test --headed --spec 'cypress/integration/TC002_Login_Spec.js'` To run specific test in chrome

#### Generate Report Locally:

- `npm run combine-reports` to combine mocha json report
- `npm run generate-report` to generate html report




