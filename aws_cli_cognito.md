# Cognito

- パスワードの強制リセット
  ```
  aws cognito-idp admin-set-user-password \
  --user-pool-id {ユーザープールID} \
  --username {ユーザー名} \
  --password {変更後のパスワード}
  ```
