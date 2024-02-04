# CloudFront

- 指定したディストリビューションのルートディレクトリ直下のキャッシュを削除
  ```
  aws cloudfront create-invalidation --distribution-id <CloudFrontディストリビューションID> --paths "/*"
  ```
