# Lambda

- 関数の一覧を表示

  ```
  aws lambda list-functions

  # 関数名だけを出力
  aws lambda list-functions --query 'Functions[*].FunctionName'
  ```
