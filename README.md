# Postman API Automation Integration with Github Actions #

This repository is a demontration for POC for integrating postman tests with github actions.The tests are writin in postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The project runs on a scheduled time with the help of the cron job.

The HTML Reports is archived and kept into artifact section for the team to download it. Along with that they can view the report drectly from the github page : https://prashantchavan3005.github.io/Phoenix-Inwarranty-flow/
The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi My Name is Prashant Chavan. I have 4.5 years of experience in Automation Testing. My Skillset Includes UI Automation with Selenium Webdriver, Playwright and for API Testing I use Rest Assured and Postman.
You can connect with me over:(https://www.linkedin.com/in/prashant-chavan-638b3019a/)

## Testing Coverage ##
1. Happy Flow Testing
2. Neagtive Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Node.js 22v
3. Newman
4. Newman-reporter-htmlextra
5. Gihub Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 instance for self hosted github runner.

## Github Pages ##
You can directly view the latest test report of the Postman test at the Github Page Link: https://prashantchavan3005.github.io/Phoenix-Inwarranty-flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/prashantchavan3005/Phoenix-Inwarranty-flow/blob/static-content/newman-report.png)


## Project Structure ##
    Phoenix Inwarranty Flow
    ├─ Inwarranty-flow Collection.postman_collection.json # Collection File
    ├─ QA.postman_environment.json #Environment File
    └─ testdata.csv # TestData File

## How to run the project? ##
You can run the project on the local system for that:
1. Clone the project on local system: https://github.com/prashantchavan3005/Phoenix-Inwarranty-flow.git
2. Install node.js and NPM from: https://nodejs.org/en/download
3. Install Newman using ``` npm install -g newman ```
4. Install neman-reporter-htmlextra using ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman command to run the collection :
    ```
    newman run 'Inwarranty -flow collection.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html 
