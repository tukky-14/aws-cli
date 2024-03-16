# awslogs

- [ターミナルから直感的に CloudWatch Logs を検索できる awslogs コマンドの紹介](https://dev.classmethod.jp/articles/show-cloudwatch-logs-with-awslogs-command/)
- 設定
  ```
  pip install awslogs
  ```

```
# 直近のLambda関数のログを取得
awslogs get /aws/lambda/MyLambdaFunction ALL

# 時間指定でLambda関数のログを取得
awslogs get /aws/lambda/MyLambdaFunction --start '2023/10/01 00:00' --end '2023/10/01 23:59'
```
