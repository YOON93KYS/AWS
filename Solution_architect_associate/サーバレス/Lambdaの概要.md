# Lambda
サーバなしで処理を実行させることが可能

## 特徴
EC2インスタンスなしでもコードの実行ができるため、効率的
- 実行基盤はAWSが管理
- AWSサービスと連携させることで簡単にイベントドリブンなアプリケーションを実行可能
- Node.js/Javaで書かれたコードを実行
- 100ミリ秒単位でコード実行時間に対して課金
- 100万回まで無料
- オートスケール

### 例えばこんな時に使えます
- CloudTrailログで異常が発生した場合、メール通知（CloudTrail→S3→Lambda→メール通知）
- Scaling処理(Kinesis Analytics→Lambda→Scaling処理)
- モバイルからの写真管理をLambdaを通じて実施するなどモバイル連携も可能
 - Cognito認証
 - S3に写真登録
 - S3に写真登録をトリガーとしてLamdba起動
 - モバイルからメタデータを取得し、DynamoDBに格納
 - Lambda実行によるメタデータをDynamoDBに登録

## Lambda@Edge
Lambdaの機能とCloudFrontのエッジロケーション処理の機能を合わせたサービス
CloudFrontにLambda機能を連携し、世界中でインフラをユーザーに近いロケーションでコードの実行が可能
### 特徴
- 性能UP
