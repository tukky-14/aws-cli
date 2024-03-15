# Lambda

- 関数の一覧を表示

  ```
  aws lambda list-functions

  # 関数名だけを出力
  aws lambda list-functions --query 'Functions[*].FunctionName'

  # 関数名だけを出力（テキスト形式で改行）
  aws lambda list-functions --output text --query 'Functions[*].[FunctionName]' | awk '{print $1}'

  # テーブル形式で表示（ファンクション名/ランタイム/メモリ/タイムアウト）
  aws lambda list-functions --query "Functions[].[FunctionName,Runtime,MemorySize,Timeout]" --output table
  ```
