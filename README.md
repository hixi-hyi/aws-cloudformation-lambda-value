# cfn-lambda-ssm-secret
## Description
The `cfn-value` function define a constant in outside `Parameter`.

## When do you use it
* Define a constant to use repeatedly in AWS::CloudFormation

## Deploy
[See here](https://github.com/hixi-hyi/aws-cloudformation-lambda#deploy)

## Usage
```
Resources:
  Domain:
    Type: Custom::Value
    Properties:
      ServiceToken: !ImportValue cfn-lambda-value:LambdaArn
      Value:
        Fn::Join:
          - "."
            - !Ref Environment
            - "example.com"
Outputs:
  OutputDomain:
    Value: !Ref Domain
```
## Parameters
### Value
- Define the value
- ***Required:*** Yes
- ***Update requires:*** Replacement

## Contributing
[See here](https://github.com/hixi-hyi/aws-cloudformation-lambda#contributing)
