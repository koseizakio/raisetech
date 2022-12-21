## EC2上にサンプルアプリケーションをデプロイして、動作させてください。


### サンプルは第3回で案内済みのものを使ってください。

※まずは組み込みサーバーだけで、動作したらサーバーアプリケーションを分けて動くかチャレンジしてみましょう。


### 動作したら、ELB(ALB)を追加してみましょう。


### ELB を加えて動作が確認できたら、さらに S3 を追加してみましょう。S3 をどのように使うかはお任せします。


## ここまでが問題無く動作したら、その環境を構成図に書き起こしてください。





### EC2のAmazon Linuxに動作する内容

EC2： koseizakio-web-01

RDS： koseizakio-db-01

```
sudo yum -y update
```
```
sudo yum remove -y mysql-server
```
```
sudo yum remove -y mariadb*
```
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
mysqlサーバー起動

```
sudo service mysqld start && sudo service mysqld status
```
gitをインストール

```
sudo yum install git
```
```
git clone https://github.com/koseizakio/raisetech-ruby-on-rails-koseizakio.git
```
```
cd raisetech-ruby-on-rails-koseizakio/
```

Ruby インストール

https://nomad.office-aship.info/amazon-linux2-rbenv-ruby-3/



rbenv をダウンロード
```
git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
```

```
git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
```

PATHの設定

```
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile
```

```
echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
```

```
source ~/.bash_profile
```

rbenv のバージョン確認

```
rbenv --version
```

インストールできる ruby のバージョン一覧

```
rbenv install --list
```

rubyのビルドに必要なライブラリのインストール

```
sudo yum install -y gcc openssl-devel zlib-devel
```

rubyのビルド

```
rbenv install 3.1.2
```

ビルドしたrubyを有効にする

```
rbenv global 3.1.2
```

bash_profile 再読み込み

```
source ~/.bash_profile
```

ruby のバージョン確認

```
ruby -v
```

bunder のバージョン確認

```
bundler -v
```



































