# AWSの全体像

# AWSサービス

## 優先度高の範囲
- アプリケーション統合
- コンピューティング
  -　優先度高
    - EC2：クラウド内で仮想サーバーを作る機能
    - EC2 Auto Scaling：EC2を自動でスケーリングする。高可用性を担保
    - AWS Lambda：イベント発生時にコード実行
    - Elastic Load Balancing：複数のターゲットに渉着信トラフィックの分類、
  - 優先度低
    - Elastic Container Service（ECS）：Dockerを使ってCI/CD継続デリバリーなど使用
    - Elastic Beanstalk：サーバー構築を一部自動化してくれて、管理してくれるところ
- データベース
  - 優先度高
    - Amazon Aurora：リレーションDBを分散型に
    - Amazon RDS：代表的なDB
    - Amazon DynamoDB：代表的なNOSQLデータベース
    - Amazon ElastiCache：インメモリキャッシングシステム
    - Amazon Redshift：高速、シンプル、コスパの良いデータウェアハウス
- マネジメントとガバナンス
  - 優先度高
    - Amazon CloudWatch
    - AWS Auto Scaling
    - AWS CloudFormation
    - AWS マネジメントコンソール
  - 優先度低
    - AWS Cloud Trail
    - AWS Config
    - AWS OpsWorks
    - AWS Service Catalog
    - AWS Systems Manager
    - AWS Truted Advisor
- ネットワーキングとコンテンツ配信
  - 優先度高
    - AmazonVPC：代表的なネットワークサービス
    - Amazon CloudFront：グローバルなコンテンツ配信ネットワーク
    - Amazon Route53：ルーティングなどを設定するとき使う。スケーラブルなドメインネームシステム（DNS）
  - 優先度低
    - Amazon API Gateway：APIを構築して管理するサービス、Lamdbaと連携したりする
    - AWS Direct Connect：AWSへの専用ネットワーク接続
    - AWS Transit Gateway：VPCおよびアカウント接続を簡単にスケール
- ストレージ
  - 優先度高
    - Amazon Simple Storage Service（S3）：一番使えるサービス、Object 形式のストレージ
    - Amazon Glacier
    - Amazon Elastic Bloc Store（EBS）：S3と並んで頻繁に使うサービス
    - Amazon Elastic File System（EFS）
    - Amazon FSx for Windows ファイルサーバー
- セキュリティ、アイデンティティ、コンプライアンス
- ネットワーキングとコンテンツ配信
  - 優先度低
    - AWS Storage Gateway：オンプレミスのデータを持ってきて保存する役割をメインとしている
## 優先度低の範囲
- 開発者ツール