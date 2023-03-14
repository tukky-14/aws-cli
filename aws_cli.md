# AWS CLI コマンドメモ

- AWS CLI の設定
  ```
  aws configure
  ```
- AWS CLI を複数アカウントで使用したい場合
  ```
  aws configure --profile <name>
  ```

<br/>

## S3

- バケット内のデータをすべて削除
  ```
  aws s3 rm s3://<S3バケット名>/ --recursive
  ```
- 指定したフォルダのデータを S3 にアップロード
  ```
  aws s3 cp <フォルダパス> s3://<S3バケット名>/ --recursive
  ```

<br/>

## API Gateway

- Cognito オーサライザーを複数設定する
  ```
  aws apigateway create-authorizer \
  --rest-api-id {API GatewayのAPI ID} \
  --name {オーソライザーの名前} \
  --type COGNITO_USER_POOLS \
  --provider-arns {Cognito UserPoolのARN1} {Cognito UserPoolのARN2} \
  --identity-source method.request.header.Authorization
  ```

<br/>

## Cognito

- パスワードの強制リセット
  ```
  aws cognito-idp admin-set-user-password \
  --user-pool-id {ユーザープールID} \
  --username {ユーザー名} \
  --password {変更後のパスワード}
  ```

<br/>

## CloudFront

- 指定したディストリビューションのルートディレクトリ直下のキャッシュを削除
  ```
  aws cloudfront create-invalidation --distribution-id <CloudFrontディストリビューションID> --paths "/*"
  ```
