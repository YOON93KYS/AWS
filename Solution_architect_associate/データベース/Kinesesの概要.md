# Kinesisの概要
ストリームデータを収集・処理するためのフルマネージド型
3つのサービスで構成されている
Amazon Kinesis Data Streamsがメインで、他は組み合わせて利用している

# Amazon Kinesis Data Streams
ストリームデータを処理するアプリケーションを構築
ex)
1.IoTのデータ取得するサービスと連動してKinesis Streamsにいれて Streams処理をする
2.Spark Streamingシステムと連携することでStreamingデータを処理・解析する
3.それと連携して、リアルタイムで処理を行うアプリケーションを構築することができる

## 処理の仕組み
ストリーミング処理をシャードに分けて分散させて実行する → 分散処理しているので高速処理が可能
Shard追加 → 速度UP

## 特徴
データ提供側（プロデューサー）とデータ利用側（コンシューマー）を繋ぐことで、様々なサービスが利用可能

### データ提供側
- Kinesis Appender
- Kinesis Producer
- Kinesis Agent
- AWS SDK
- Cloud Watch
- Fluentd
- AWS IoT

### データ利用側
- Kinesis Firehose
- Kinesis Client
- Kinesis Analytics
- Lambda
- EMR
- Apache Storm

## 追加機能
- Amazon Kinesis Agent：データを簡単に収集して Kinesis Data Streamsに転送できる独立型 Java software application
- Amazon Kinesis Producer Library（KPL）
- Fluent plugin for Amazon Kinesis
- Amazon Kinesis Data Generator(KDG)
- Amazon Kinesis Client Library（KCL）

# Amazon Kinesis Data Firehose
ストリームデータをS3やRedshiftなどへ簡単に配信できる
Lambdaと連携するとETLとして機能する


# Amazon Kinesis Data Analytics
ストリームデータ（Kinesis Firehose、Kinesis Streamsなど）を標準的なSQLクエリでリアルタイムに可視化・分析

解析した結果をKinesis Firehose、Kinesis Streamsに返すこともできる

# 単語整理
- シャード(Shard):ストリーム内の一意に識別されたデータレコードのシーケンス
- シーケンス（Sequence）：順番