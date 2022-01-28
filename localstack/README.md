
# Deploy 
```
devspace deploy
```

## Install LocalStack 
<br>

Follow [LocalStack AWS CLI](https://docs.localstack.cloud/integrations/aws-cli/#localstack-aws-cli-awslocal)


# Usage

### Create new AWS resources

1. Connect and forward container ports by running: 
    ``` 
    devspace dev 
    ``` 
2. Use ```awslocal``` to create resources
 
    #### Examples:

    New Kinesis stream:

    ``` 
    awslocal kinesis create-stream --stream-name new-stream --shard-count 1
    ```
    New SNS Topic:
    ```
    awslocal sns create-topic --name new-topic
    ```

    New SQS: 
    ```
    awslocal sqs create-queue --queue-name new-queue
    ```

### How to use it in your services

Set ```AWS_ENDPOINT``` to ``` http://localstack:4566 ```