# 第3回　講座・課題で学んだこと

## APサーバーについて

- APサーバー名称：Puma
- バージョン：5.6.5
- APサーバー終了時：アクセスできなくなる

## DBサーバーについて

- DBサーバー名称：MySQL
- バージョン：8.0.34
- DBサーバー終了時：アクセスできなくなる

## 構成管理ツールについて

- 名称：Bundler
- バージョン：2.3.14

## サンプルアプリ入手からデプロイまで実際の手順

1. サンプルアプリの入手　git clone https:~
2. Ruby 3.1.2のインストール　rvm install 3.1.2
3. MySQLのセットアップ＆初期パスワードの変更　https://github.com/MasatoshiMizumoto/raisetech_documents/blob/main/aws/docs/install_mysql_on_cloud9_amazon_linux_2.md
4. Rails 7.0.4のインストール gem install rails -v '7.0.4'
5. Bundlerのインストール　gem install bundler -v 2.3.14
6. Yarnのインストール　npm install -g yarn@1.22.19
7. database.yml ファイルの作成および編集
　database.ymlファイルがなかったためdatabase.yml.sampleファイルをコピーして作成　
　mysql_config --socketでソケットの場所を確認→socketの項目に入力
　passwordには設定したMySQLのパスワードを入力
8. bundle install を実行
9. bin/setup　で環境構築を実行
10. bin/cloud9_devで起動
11. エラーが出るのでその内容にあわせてconfig/environments/development.rb ファイルを編集する
    →endの前にconfig.hosts << "~~"を入力して接続を許可する
12. 再度bin/cloud9_devで起動　※画像が上手く表示されない時はsudo yum install  -y  ImageMagick
![デプロイしたアプリのスクショ](./20230823-RaiseTech-task/サンプルアプリデプロイ.png)
