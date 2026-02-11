# ローカルでの起動コマンド
```bash
$ docker build -t my-html-image .
docker run -d -p 8080:80 my-html-image
```

# CI/CD with CodePipeline + CodeBuild + ECS (Fargate)

## 要件

* GitHub への push をトリガーに自動デプロイ
* CodeBuild で Docker イメージをビルド
* Amazon ECR に push
* Amazon ECS (Fargate) に自動デプロイ
* ブラウザからアプリにアクセス可能にする
