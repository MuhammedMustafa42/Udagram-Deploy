# Udagram Hosting:

- i didn't hard-code the environment variables i added them to circleCi instead and passed them through code to the deployment environment using deploy.sh file.

- package.json has all the scripts for installation , build test and deployment for both backend and frontend.

## Pipeline process:
### Continuous integration:
- added the neccessary jobs for installing and building the frontend and backend for the application in the package.json files and then called these scripts inside the main package.json file for the app.

- added the jobs inside circleci config.yml file for installing dependencies using `npm run frontend:install` and `npm run backend:install` commands.

- added the jobs for building the application both frontend and backend using `npm run frontend:build` and `npm run backend:build` commands.

### Continuous deployment:
- added all the commands needed for deploying the app in package.json files for both frontend and backend and called theses scripts in the main package.json file for the application.

- added elasticbeanstalk and aws in circleci orbs for setting and installing.

- added the neccessary jobs for deploying the frontend and backend for the application inside circleci yml file by calling the deploy scripts that was aaded to the main package.json file.

- linked github to circleci so that circleci will be triggered if any pushes happen to github.

- The badge: [![CircleCI] (https://circleci.com/gh/circleci/circleci-docs.svg?style=svg)](https://app.circleci.com/pipelines/github/MuhammedMustafa42)