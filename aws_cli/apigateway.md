# API Gateway

- Cognito オーサライザーを複数設定する
  ```
  aws apigateway create-authorizer \
  --rest-api-id {API GatewayのAPI ID} \
  --name {オーソライザーの名前} \
  --type COGNITO_USER_POOLS \
  --provider-arns {Cognito UserPoolのARN1} {Cognito UserPoolのARN2} \
  --identity-source method.request.header.Authorization
  ```
