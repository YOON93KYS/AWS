# AWS KMS
AWS KMSは簡単にデータを暗号化するためのマネージド型暗号化サービス
RDSでは保存されるデータ・リソースのアンコウかと接続の暗号化を実施可能

## カスタマーマスターキー
- 暗号化を実施する上で、最初に作成されるマスターキー
- 暗号化キーをアンコウかする
- ローテーションされる
## カスタマーデータキー
- 実際のデータの暗号化に利用するキー
- KMSで生成されてCMKで暗号化される
## エンベロープ暗号化
- マスターキーで暗号化をせずに、暗号化したデータキーを利用して暗号化する暗号化方式
  - データキーとマスターキーによる暗号化を実施
  - カスタマーマスターキー（CMK）を利用してデータキーを暗号化する
  
　