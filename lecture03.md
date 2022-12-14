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


