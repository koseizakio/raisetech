# 第３回 課題

※Cloud9のEBSを10GBから40GBに変更
※円滑に動かすため<strong>t3.small</strong>インスタンスで起動

### yumのアップデート

```
sudo yum -y update
```

###  mariadbがある場合を想定して先に削除
```
sudo yum remove -y mysql-server
```
```
sudo yum remove -y mariadb*
```

###  "https://dev.mysql.com/get/mysql80-community-release-el7-7.noarch.rpm" をダウンロード

```
wget https://dev.mysql.com/get/mysql80-community-release-el7-7.noarch.rpm
```

```
sudo yum localinstall -y mysql80-community-release-el7-7.noarch.rpm
```
```
sudo yum install -y mysql-community-devel 
```

```
sudo yum install -y mysql-community-server
```

・MySQLサーバーの起動＆確認

```
sudo service mysqld start && sudo service mysqld status
```

・初期パスワードの確認

```
sudo cat /var/log/mysqld.log | grep "temporary password" | awk '{print $13}'
```

・ログイン確認

```
mysql -u root -p
```

・ログイン確認

```
mysql -u root -p
```

・rvm（Ruby Version Manager）を利用すれば、さまざまなバージョンのRubyを指定してインストールできます
```
rvm get stable
rvm install 3.1.2
rvm --default use 3.1.2
```

・Rubyドキュメントをスキップする設定を.gemrcファイルに追加するコマンド
```
echo "gem: --no-document" >> ~/.gemrc
```

バージョンを指定してRailsをインストールする
```
gem install rails -v 7.0.4
```

bundlerのバージョンを指定してインストールする
```
gem install bundler -v 2.3.14
```

![database.yum　の変更部分](./img/lecture03_01.png)

### MYSQLの変更部分
```
koseiozaki:~/environment/raisetech-live8-sample-app (main) $ mysql -u root -p                                   
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 19
Server version: 8.0.31

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> SET PASSWORD = '<2nzDqdZ.d=r';
Query OK, 0 rows affected (0.02 sec)

mysql> exit;
Bye
koseiozaki:~/environment/raisetech-live8-sample-app (main) $ rails db:createRunning via Spring preloader in process 19704
Created database 'raisetech_live8_sample_app_development'
Created database 'raisetech_live8_sample_app_test'
koseiozaki:~/environment/raisetech-live8-sample-app (main) $ rails db:migrate
Running via Spring preloader in process 19860
== 20210129231905 CreateFruits: migrating =====================================
-- create_table(:fruits)
   -> 0.0292s
== 20210129231905 CreateFruits: migrated (0.0293s) ============================

== 20211003014450 CreateActiveStorageTables: migrating ========================
-- create_table(:active_storage_blobs)
   -> 0.0347s
-- create_table(:active_storage_attachments)
   -> 0.0422s
-- create_table(:active_storage_variant_records)
   -> 0.0373s
== 20211003014450 CreateActiveStorageTables: migrated (0.1148s) ===============

```


