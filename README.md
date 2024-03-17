# AWS CLI コマンドメモ

- AWS CLI の設定

```bash
aws configure
```

<br/>

- AWS CLI を複数アカウントで使用したい場合

```bash
aws configure --profile <name>
```

<br/>

- 現在 AWS CLI に設定されているアカウント情報の取得

```bash
aws sts get-caller-identity
```
