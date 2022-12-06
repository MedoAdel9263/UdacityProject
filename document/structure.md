### AWS

* This website is being hosted on AWS.
* Elastic Beanstalk is used to set up the Backend API.
* S3 bucket for hosting frontend.
* RDS database running Postgres.

## high-level overview of the infrastructure

![overview](./screenshots/Diagram/structure.png)

### FrontEnd Enviroment: 

* S3 BucketName: udagram-front
    
    S3 URL: `http://mymadelbucket.s3-website-us-east-1.amazonaws.com/`

### BackEnd Enviroment: 

## DataBase

# AWS RDS (postgres)

DB ENDPOINT: `database-1.cbegjmn3bd4o.us-east-1.rds.amazonaws.com`

![RDS](./screenshots/RDS/database.png)

* RDS Test connection

![RDS Test connection](./screenshots/RDS/database_connection.png)

## Elastic Beanstalk

* Application Name [EB_APP]: udagram-api
* Enviroment Name [EB_ENV]: contact-api-dev

    EB URL: `http://contact-api-dev.eba-brmau8q8.us-east-1.elasticbeanstalk.com`


### Deployment Pipeline Enviroment:

* CircleCI
* GitHub Repo: `https://github.com/MedoAdel9263/UdacityProject`