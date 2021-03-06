# AWSの仕組み
インフラ/システム機能をブロックパーツのようにオンライン上に組み合わせて自分の好きな構成を表現する仕組み


* VPCのネットワークから外のネットワークに繋ぐ時、Route53（DNS）設定をすればOK

## アンマネージド型
- スケーリング/耐障害性/可用性を利用者側に設定し管理する必要がある
- 代表的なサービス：EC2（サーバー）

### メリット
- 設定が柔軟に可能
### デメリット
- 管理が面倒

## マネージド型
- スケーリング/耐障害性/可用性がサービスに組み込まれておりAWS側で管理されている
- 代表的なサービス：Route53（DNS）
### メリット
- 管理が楽
### ディメリット
- 設定が限定的

# AWSのグローバルインフラ構成
リージョンとアベイラビリティーゾーン（Availability Zone）とエッジロケーション3つの区分


## リージョン
リージョンは国や地域における地理的に隔離されたAWS拠点

- 前提：物理的に独立したインフラ拠点
- ただし、隣接リージョン間は広帯域の専用ネットワークで接続されている

* 広帯域（こうたいいき）：ブロードバンド
- リージョンに応じてAWSサービスの値段が違う

## アベイラビリティーゾーン（Availability Zone）
- 同リージョン内のAZ同士は低レイェンションーのリンクで接続されている
- AZは1つの複数の物理的なデータセンターで構成されている
- AZにある物理インフラを仮想化してユーザーにインフラ機能をサービスとして提供している

## エッジロケーション
エッジロケーションはキャッシュデータなどを利用する際の更に小さなエンドポイントとなる拠点

ex) CloudFront、Lambdaエッジ

