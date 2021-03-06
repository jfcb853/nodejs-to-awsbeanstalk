# nodejs-to-awsbeanstalk
 NodeJs app to deploy to AWS beanstalk

### Status:
[![CircleCI](https://circleci.com/gh/jfcb853/nodejs-to-awsbeanstalk.svg?style=svg)](https://app.circleci.com/pipelines/github/jfcb853/nodejs-to-awsbeanstalk)

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/jfcb853/nodejs-to-awsbeanstalk/blob/master/LICENSE)

## Pipeline

NodeJS app --> Github --> AWS CodePipeline --> AWS Elastic BeanStalk 

## App details
 NodeJs app running on port 5000

 # Notes:
 - add this to the app.js file
 ```sh
 const port = process.env.port || 5000;
```
 - Add package json also add the "start" script: 
 ```sh
 "start" : "node src/app.js",
 ```

## things to check at AWS CodePipeline
A IAM Role Service was created by Pipeline:
AWSCodePipelineServiceRole-us-west-2-sharks-nodejs

## things to check at AWS BeanStalk
- Add AWS Elastic BeanStalk check the logs where the EBS is runnign the app ( exmaple 8080) , and add this to COnfiguration --> software , Environment as:
    port  8080

    Apply the changes.

- Adding CircleCI Integration
 * config.yml file created 

- Additional things to do for exmaple
 * add test with supertest and mocha for example

