# S3

- バケットの一覧を表示

  ```
  aws s3 ls
  ```

- バケット内のデータをすべて削除
  ```
  aws s3 rm s3://<S3バケット名>/ --recursive
  ```
- 指定したフォルダのデータを S3 にアップロード

  ```
  aws s3 cp <フォルダパス> s3://<S3バケット名>/ --recursive
  ```

- S3 バケット内の指定したフォルダの移動

  ```
  aws s3 mv s3://<S3バケット名>/ s3://<S3バケット名>/ --recursive
  ```

- コマンドを確定させず、実行した場合の結果だけ表示させるオプション
  ```
  --dryrun
  ```

<br/>

- [AWS CLI での高レベル (S3) コマンドの使用](https://docs.aws.amazon.com/ja_jp/cli/latest/userguide/cli-services-s3-commands.html)
- [AWS CLI サポート対象のコマンド](https://docs.aws.amazon.com/ja_jp/snowball/latest/developer-guide/using-adapter-cli.html)
