## EC2上にサンプルアプリケーションをデプロイして、動作させてください。


### サンプルは第3回で案内済みのものを使ってください。

※まずは組み込みサーバーだけで、動作したらサーバーアプリケーションを分けて動くかチャレンジしてみましょう。


### 動作したら、ELB(ALB)を追加してみましょう。


### ELB を加えて動作が確認できたら、さらに S3 を追加してみましょう。S3 をどのように使うかはお任せします。


## ここまでが問題無く動作したら、その環境を構成図に書き起こしてください。





### EC2に書き込むユーザーデータ

```
sudo yum -y update

sudo yum remove -y mysql-server

sudo yum remove -y mariadb*

wget https://dev.mysql.com/get/mysql80-community-release-el7-7.noarch.rpm

sudo yum localinstall -y mysql80-community-release-el7-7.noarch.rpm

sudo yum install -y mysql-community-devel 

sudo yum install -y mysql-community-server

sudo service mysqld start && sudo service mysqld status

curl -L get.rvm.io | bash -s stable

rvm get stable

rvm install 3.1.2

rvm --default use 3.1.2

echo "gem: --no-document" >> ~/.gemrc

git clone https://github.com/yuta-ushijima/raisetech-live8-sample-app.git

gem install rails -v 7.0.4

gem install bundler -v 2.3.14

bundle install

nvm install 14

nvm use 14

npm install -g yarn


```
