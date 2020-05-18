### My first Serverless Endpoint using the Serverless Framework


#### Prerequisites: 
1. AWS Account
2. Account in https://serverless.com


#### Steps:

1. Create initial template:
```
$ serverless create --template aws-nodejs
```

2. Attach an event to the Lambda function which will trigger function and update other required properties like app, org etc in the serverless.yml file

3. Login to severless account
```
$ sls login
```

4. Deploy
```
$ serverless deploy
```
What it does in the background for us:
```
Serverless: Creating Stack...
Serverless: Stack create finished...
Serverless: Uploading CloudFormation file to S3...
Serverless: Uploading artifacts...
Serverless: Uploading service hello-serverless.zip file to S3 (121.23 KB)...
Serverless: Uploading custom CloudFormation resources...
Serverless: Validating template...
Serverless: Updating Stack...
Serverless: Stack update finished...

Service Information
service: hello-serverless
stage: dev
region: us-east-1
stack: hello-serverless-dev
resources: 18
api keys:
  None
endpoints:
  GET - https://xxxxxxx.execute-api.us-east-1.amazonaws.com/dev/hello
functions:
  hello: hello-serverless-dev-hello
layers:
  None
Serverless: Publishing service to the Serverless Dashboard...
Serverless: Successfully published your service to the Serverless Dashboard: https://dashboard.serverless.com/tenants/xxxxx/applications/serverless-hello-app/services/hello-serverless/stage/dev/region/us-east-1
```



Ref: https://www.serverless.com/learn/courses/full-stack-application-development-on-aws/