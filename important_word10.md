# はじめに押さえておきたい！初学者向け AWS キーワード Top 10
- URL : https://www.youtube.com/watch?v=VIpulFnarKQ

## Availability Zone
- リージョン
  - AWSが稼働している場所・地域
  - リージョンをグローバルネットワークで結んで高速なネットワークで繋ぐ
- Availability Zone
  - リージョンの中に存在するサーバ群
  - 1個のAvailability Zoneが壊れても、別のAvailability Zoneが動くため、障害に強いサーバとなる
- マルチAZ構成
  - 複数のAvailability Zoneにまたがった構成とすることで高い可用性を実現する

## Black Belt
- Black Belt Online Seminer というオンラインセミナーの名前
- 動画で受講できるオンデマンド方式
- AWS black beltで検索
  - サービス別資料を閲覧可能

## Amazon VPC
- VPC = Virtual Private Cloud
- お客様専用の独立したネットワーク環境を整えることが可能
- Availability Zoneにまたがってネットワークを構成することが可能

## AWS STS / AWS IAM
- セキュリティに関連する
- AWS IAM
  - 認証・認可の仕組み
  - あなた誰？：認証、この資材にアクセス可能？：認可
- AWSのルートアカウント
  - 自分のメアドとパスワードで作成したユーザ
  - 権限が強すぎるので使いすぎない
- IAMの構成要素
  - IAMユーザ：運用者1人1人に割り当てる
  - IAMポリシー：どのAWSリソースに何ができるかを定義（認可）
  - IAMグループ：IAMユーザを一括で管理して、ポリシーを付与
  - IAMロール：一時的に権限を渡す
- AWS STS(Security Token Service)
  - 一時的にトークンを払いだす
  - IAMロールと共に用いて、サービス間のセキュリティを担保する
  - 一時的な鍵であるため、プログラムの共有時に情報漏洩のリスクを減らせる