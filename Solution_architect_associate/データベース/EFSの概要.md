# EFS(Elastic File System)
複数のEC2インスタンスからアクセス可能な共有ストレージ

## S3
大容量のデータを長期保存するためのもの

## EBS
複数のEC2インスタンスにアタッチできない

## EFS（Elastic File System）
- NASに似たファイルストレージ
- ファイルシステムとして利用し、複数のEC2インスタンスでの共有アクセスが可能

# EFSの特徴
## シンプル
- フルマネージド型サービス
- NFSv4プロトコルを利用して、関連ツールや標準プロトコル/APIでアクセス可能
## スケーラブル
- ペタバイトまでスケーラブルにデータを蓄積
## 柔軟性
- ファイルの減少に合わせて自動で拡張・축소
- 事前に容量を設定する必要なし
- 使った分だけ課金

## 基本性能
何千も同時アクセスが実現可能という性能が特徴的

## EFSのデータ保存
EFSのデータファイルは複数AZに分散して保存されている

## EFSの設定
EFS構築では以下の設定を実施する
- ファイルシステムを作成
 - ファイルシステム：EFSの管理単位でファイルやディレクトリの保管場所。
- 接続先のマウントターゲットの作成
 - マウントターゲット
  - EC2インスタンスからの接続先のマウントターゲットを設定
  - EC2インスタンスからマウントターゲットを介して、AZ外にあるEFSにアクセスできる
  - 複数AZにある複数ECインスタンスからEFSにアクセスできる
- セキュリティグループの作成
- パフォーマンスモードの選択
 - 汎用モードと最大I/Oモードから選択。基本は汎用モード

## バースト機能
ファイルストレージの負荷に対してバースト機能によってスケーラブルに対応

## EFSクライアント
EFSをEC2インスタンスから操作する際に専用のクライアントソフトウェアを利用する

