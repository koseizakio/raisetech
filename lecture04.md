# 第４回 課題

今回は、AWSの https://catalog.us-east-1.prod.workshops.aws/workshops/47782ec0-8e8c-41e8-b873-9da91e822b36/ja-JP を元に第４回の課題を行なった。

構成は、東京リージョンでアベビラリティーゾーンAでEC2とRDSを一つずつ作成した。

## AWS上に新しくVPCを作ってください。

### VPC 作成

![スクリーンショット 2022-12-20 0 11 25](./img/lecture04_01.png)

### サブネット

![スクリーンショット 2022-12-20 0 12 59](./img/lecture04_02.png)

### セキュリティグループ

PC から EC2へのセキュリティグループ
![スクリーンショット 2022-12-20 0 14 35](./img/lecture04_03.png)

EC2 から RDSヘのセキュリティグループ
![スクリーンショット 2022-12-20 0 14 44](./img/lecture04_04.png)


## EC2 と RDS を構築してください

### EC2の構築結果

![スクリーンショット 2022-12-20 0 20 32](./img/lecture04_05.png)

### RDSの構築結果

![スクリーンショット 2022-12-20 0 21 58](./img/lecture04_06.png)

### EC2とRD2でWordPress初期構築画面

![スクリーンショット 2022-12-19 23 59 07](./img/lecture04_07.png)



## EC2 から RDS へ接続をし、正常であることを確認して報告してください。

![スクリーンショット 2022-12-19 23 58 15](./img/lecture04_08.png)

参考にしたサイト

https://blog.serverworks.co.jp/ec2-to-private-rds








