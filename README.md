## Serverless REST API with DynamoDB
This is a sample REST API built using the Serverless Framework with AWS Lambda and DynamoDB.

## Requirements
- Node.js
- Serverless Framework
- AWS CLI

## Installation
Install the required Node.js packages.
```
nvm use latest
```

Deploy the application using the Serverless Framework.
```
serverless deploy --stage dev
```

Create a new item in the DynamoDB table.
```
aws dynamodb put-item --table-name sample-api-items --item '{"id": {"S": "1"}, "name": {"S": "Item 1"}, "description": {"S": "This is item 1."}}'
```

## Usage
After deploying the application and adding an item to the DynamoDB table, you can test the API by sending HTTP requests to the generated endpoints.

## Cleanup
You can remove all resources created by the Serverless Framework using the following command.

```
serverless remove --stage dev
```
