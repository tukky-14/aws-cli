# DynamoDB

- テーブルの一覧を表示

  ```
  aws dynamodb list-tables
  ```

- テーブルに関する情報の取得

  ```
  aws dynamodb describe-table --table-name diary
  ```

- テーブルのスキャン

  ```
  aws dynamodb scan --table-name diary
  ```

- レコード数のカウント
  ```
  aws dynamodb scan --table-name diary --select "COUNT"
  ```
