 # IAM設計
 AWSを利用するユーザーの役割やアクセス権限を自社の組織構造と合わせて設計することが重要

 ## IAMユーザー or IAMグループ
 少数利用はIAMユーザーを組織利用はIAMグループを設定する
 少数利用がずっと継続する場合を除いて、少数利用も含めて最初からIAMグループで設定する方が良い

 ## グループ設計
 組織別または個人単位にAWS利用者とその役割別の利用範囲を生理して、グループ設計を実施する
 ### AWS利用者と役割の洗い出し
 - AWS利用者の特定
 - 利用者の役割と利用範囲を生理
 ### 利用グループへと集約
 - 同じ役割や利用反映を1つのグループとしてまとめる
 - グループ別の名称と最小限利用範囲を確定する