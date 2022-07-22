# Hosting a Full-Stack Application

## Deploying udagram project

- The configuration files are updated to set the environment variables to the project code, for example setting the server port and server url and database port, database url, user and password. It's in udagram-api/src/config/config.ts
- Add all the scripts inside the package.json file. I added scripts for installation, build and deployment for both backend and frontend to automate all the steps.
- Add screenshots for all aws resources and environments.
- For accessing the application please visit: 'http://udagram2022.s3-website-us-east-1.amazonaws.com/' but please make sure you are using a browser that doesn't enforce CORS policy or blocking the user of the EB aws URL by the S3 URL.
- for accessing my github repository which is linked to circleci, pleaase visit: 'https://github.com/ehabpop/udagram-deployment'

## pipeline process inside circleci.

## Continuous integration

- First add command for installing and building the application in package.json files in the frontend and backend then call these scripts inside package.json file of the main application>
- Second add the jobs inside circleci config.yml file for installing all the dependenceis on both the frontend and backend using: 'npm install' command inside package.json files.
- Third add the jobs for building the frontend and backend by calling the corresponding scripts.

### Continuous Deployment:

- First add all the commands needed for deploying the application in the package.json files in the frontend and backend the call these scripts inside the package.json file in the main application.
- Second add the Elastic Beanstalk and aws in the circleci orbs for setting them up and installing them for deplyment.
- Third add jobs inside circleci yml file for deploying the frontend and the backend just by calling the deploy scripts added to the main package.json file which calls the deploy commands added the the package.json file fot both the frontend and backend.
- I linked mu github repository to circleci and specified the branch og interest to main branch so circleci in only triggred if the code pushed to the main branch.

## All the screenshots for the EB and S3 and DB and circleci are added to the zip file and the corresponding directory.
