# 第３回 課題

※Cloud9のEBSを10GBから40GBに変更
※円滑に動かすため<strong>t3.small</strong>インスタンスで起動

```
# yumのアップデート
sudo yum -y update
```

```
# mariadbがある場合を想定して先に削除
sudo yum remove -y mysql-server
sudo yum remove -y mariadb*
```

```
# "https://dev.mysql.com/get/mysql80-community-release-el7-7.noarch.rpm"をダウンロード
wget https://dev.mysql.com/get/mysql80-community-release-el7-7.noarch.rpm

sudo yum localinstall -y mysql80-community-release-el7-7.noarch.rpm
sudo yum install -y mysql-community-devel 
sudo yum install -y mysql-community-server
```



