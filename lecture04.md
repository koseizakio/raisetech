# 第４回 課題

今回は、AWSの https://catalog.us-east-1.prod.workshops.aws/workshops/47782ec0-8e8c-41e8-b873-9da91e822b36/ja-JP を元に第４回の課題を行なった。

構成は、東京リージョンでアベビラリティーゾーンAでEC2とRDSを一つずつ作成した。

## AWS上に新しくVPCを作ってください。

### VPC 作成

![スクリーンショット 2022-12-20 0 11 25](https://user-images.githubusercontent.com/39989928/208457336-1c47c830-b634-4c89-b4de-830a20909705.png)

### サブネット

![スクリーンショット 2022-12-20 0 12 59](https://user-images.githubusercontent.com/39989928/208457696-b21abe49-1fd1-4513-88fe-00be0e0af4cc.png)

### セキュリティグループ

PC から EC2へのセキュリティグループ
![スクリーンショット 2022-12-20 0 14 35](https://user-images.githubusercontent.com/39989928/208458102-02344e6d-e16b-4cc7-badf-afe5a247167c.png)

EC2 から RDSヘのセキュリティグループ
![スクリーンショット 2022-12-20 0 14 44](https://user-images.githubusercontent.com/39989928/208458198-c4746018-1f26-4679-85af-a841bcdffc25.png)


## EC2 と RDS を構築してください

### EC2の構築結果

![スクリーンショット 2022-12-20 0 20 32](https://user-images.githubusercontent.com/39989928/208459413-13652e39-9249-4de1-9026-5ae9c604310d.png)

### RDSの構築結果

![スクリーンショット 2022-12-20 0 21 58](https://user-images.githubusercontent.com/39989928/208459599-5baaef52-fab4-4563-8af9-57ca2b8d0be5.png)

### EC2とRD2でWordPress初期構築画面

![スクリーンショット 2022-12-19 23 59 07](https://user-images.githubusercontent.com/39989928/208459729-4054757f-1424-4b4a-8d46-7e283883d32a.png)



## EC2 から RDS へ接続をし、正常であることを確認して報告してください。

![スクリーンショット 2022-12-19 23 58 15](https://user-images.githubusercontent.com/39989928/208459891-57e06f5c-43b0-42e1-a0c6-d7504297ca46.png)

参考にしたサイト

https://blog.serverworks.co.jp/ec2-to-private-rds








