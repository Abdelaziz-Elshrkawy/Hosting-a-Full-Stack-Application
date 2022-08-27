# Udagram Project Documentation 

## Infrastructure (SErvices used to start CI/CD Pipline)
###    - AWS RDS (Relational Database Service) Using PSQL (POSTGRESQL)=> The RDS is just a database used by website to store and retrieve data
###    - AWS S3 (Simple Storage Service) => used to store the Client side files and initialize endpoint for it.
###    - AWS EB (Elastic Beanstalk)=> Is Easy to use service uses AWS S3 service to store the data and mainly used for archiving versions of the website server and deploying server with endpoint 
###    - CircleCi => online CI (Continuos Integration) tool used for automation of of building, testing and deploying of web projects by using pipeline file (`yml` file) with sequence of jobs to do 

______________________________________________________________

## Dependencies (Packages used to build the project)
###    - Nodejs v16.0.0 While older versions can work it is advisable to keep node to latest LTS version
###    - npm V8.11.0 or more recent, Yarn can work but was not tested for this project
###    - Express V4.16.4 nodejs web framework
###    - Postgresql database V14.4 


______________________________________________________________

![Pipline](pipline-diagram.png)
## Pipeline (The sequence of build and deploy of project)
###    - First the developers start to build the project blocks and then start to test it locally
###    - after local approval the developers start to write the pipeline and create [Github](https://github.com/) repository and configure it with [CircleCi](https://app.circleci.com/) to track the changes and automate the CI/CD process
###    - while project continuos development when pushing the new changes to [Github](https://github.com/) repository the [CircleCi](https://app.circleci.com/) starts the pipeline process by following the [config.yml](../.circleci/config.yml) jobs and it uses the environment variables by inserting it on [CircleCi Environment Variables Section](../Screenshots/env-var.png)
###    - after the pipeline finishes successfully of building the client-side and server-side it starts the deployment process starting by client side if the client side deployed successfully then it will start deploying the server-side if it completed successfully the pipeline is completed and every thing to this point is good 
###    - after deploying it is important to check the website functionality by visiting the website url and trying website features.

______________________________________________________________

## Project Links

### [forntend link (website link)](http://udagram-bucket-07.s3-website-us-east-1.amazonaws.com)

### [backend link (server link)](http://udagram-api-dev2222222.us-east-1.elasticbeanstalk.com)
### database link (RDS service link):(`postgresql://postgres:postgres@database.czq5bd7etjyf.us-east-1.rds.amazonaws.com:5432/postgres`)