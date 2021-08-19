# VPCとの接続

## VPCとのオンプレミス接続

### VPN接続

### Direct Connect
お客様のデータセンターやオフィスを専用線などを介してAWSへプライベートに接続するサービス

#### メリット
- 安価なアウトバウンドトラフィック料金
- ネットワーク信頼性が高い

#### 仕組み
Direct Connectロケーションに物理的に自社オンプレ環境を接続することでAWS環境との専用線接続を実現する

### Direct Connect gateway
Direct Connect gatewayにより、同一アカウントに所属する複数リージョンの複数AZから複数リージョンの複数VPCに接続

## VPNとのDirect Connect