# Cognito

- ユーザープール情報の確認

  ```
  aws cognito-idp list-user-pools --max-results 20
  ```

<br/>

- ユーザの作成

  ```
  aws cognito-idp admin-create-user \
  --user-pool-id "ap-northeast-1_XXXXX" \
  --username "hogefuga@example.com" \
  --user-attributes Name=email,Value="hogefuga@example.com" Name=email_verified,Value=true \
  --message-action SUPPRESS
  ```

<br/>

- パスワードの強制リセット
  ```
  aws cognito-idp admin-set-user-password \
  --user-pool-id {ユーザープールID} \
  --username {ユーザー名} \
  --password {変更後のパスワード}
  ```
