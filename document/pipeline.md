### FrontEnd Deploy Script: 

    aws s3 cp --recursive ./www s3://mymadelbucket/

# S3 Frontend (mymadelbucket)

![S3 Frontend](./screenshots/S3/s3_front.png)

### BackEnd Deploy Script:
 
    - eb init contact-api-dev --platform node.js --region us-east-1

    - npm run build

    in ./elasticbeanstalk/config.yml add :
    deploy:
    artifact: www/Archive.zip

    - eb create --sample contact-api-dev
    - eb use contact-api-dev
    - eb deploy

# Elastic Beanstalk

![Elastic Beanstalk](./screenshots/Elasticbeanstalk/eb1.png)

# Elastic Beanstalk Health

![Elastic Beanstalk Health](./screenshots/Elasticbeanstalk/eb2.png)

    
### Pipeline Jobs: 

## 1- Install Dependencies for Front & BackEnd Commands:
    
   - cd udagram-api && npm install
   - cd udagram-frontend && npm install -f

# Pipeline diagram

![Pipeline diagram](./screenshots/Diagram/ci-cd.png)

# Pipline main steps

![pipline - main - steps](./screenshots/Circle-ci/pipeline.png)

    
## 2- Build BackEnd & FrontEnd Commands:
    
   - cd udagram-api && npm build
   - cd udagram-frontend && npm build

# CircleCI Build steps

![CircleCI - Build - steps](./screenshots/Circle-ci/Build.PNG)


## 3- Deploy FrontEnd & BackEnd Commands:
   
   - cd udagram-api && npm deploy
   - cd udagram-frontend && npm deploy

# CircleCI Deploy step

![CircleCI - Deploy - steps](./screenshots/Circle-ci/deploy.PNG)


## CircleCI Environment Variables

![CircleCI - Environment - Variables](./screenshots/Circle-ci/env_variables.png)