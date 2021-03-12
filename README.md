# api-backend

This repository contains a SAM template that launches a REST Api in ApiGateway, a DynamoDB table, and 2 simple Lambda functions that can read from and write items to the DynamoDB table.

Once the stack has been launched you can find the invocation URL in the CloudFormation console -> Outputs tab -> ApiEndpoint

## Create a new item, or replace an old item with a new item

```
URL: {ApiEndpoint}
Method: POST
Body: JSON object that contains the key "id". All values must be strings.
      E.g. {"id": "3", "Name": "whale", "NumLegs": "0"}
```

Where {ApiEndpoint} is the value from the CloudFormation stack Outputs

e.g. https://l2kubgumhl.execute-api.ap-southeast-2.amazonaws.com/dev/

## Get Item by id

```
URL: {ApiEndpoint}/id/{id}
Method: GET
```

Where {id} is the ID of the item you would like to retrieve

E.g. https://l2kubgumhl.execute-api.ap-southeast-2.amazonaws.com/dev/id/3
