### The Application itself:

- first I added all the commands needed for installing, building and deploying the application.
- second writting the jobs inside circleci config.yml file for installing all the dependencies on bothe the frontend and backend using: 'npm install' command inside package.json files>
- Then added the jobs for building the frontend and backend by calling the correspoding scripts.

### AWS Deployment

- RDS Postgres database instance that has the database structure with all the data content and linked to backend code (inside Elastic Beanstalk).
- Elastic Beanstack environment the handles the application environment and sends requests to RDS database and recevies the request to be sent to the frontend inside S3 to display the relevant webpages to the user.
- S3 that holds the frontend files which also sends the requests to the backend to be handeled and renders the HTML pages returned as a response displayed to user.

### The Architecture Diagram is added showing the communication between these different services and infrastructure.

### The screenshots of the instances created in the aws services are added to the infrastructure directory as well.
