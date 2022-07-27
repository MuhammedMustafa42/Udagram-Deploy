### The App:
- added all the commands needed for installing, testing and building the app in the package.json files.

- added the jobs inside circleci config.yml file for installing the dependencies using `npm install` command and also the jobs for building the frontend and backend using `npm run build`.

### AWS Deployment:
- RDS postgres database: provides database structure to store all the data content and it is linked to the backend code.

- Elastic Beanstalk environment: provide an environment that handles the application environment and sends requests to and receives responses from RDS database to be sent to the client side inside S3 to be displayed to the user.

- S3 bucket: provide buckets that holds the frontend files and sends requests to the backend and renders the HTML pages as a response to be displayed to the user.
