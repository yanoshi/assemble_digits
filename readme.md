# Vagrant + Chef(Docker)でDigitsを立てるやつ
## 概要
caffeのフロントであるDigitsをさくっと建てるVagrantfile等一式です。

http://nametake-1009.hatenablog.com/entry/2016/07/07/011433

ちなみに`docker-compose.yml`はHatenaID:nametake-1009氏のブログから頂戴しました。多謝。

http://nametake-1009.hatenablog.com/entry/2016/07/07/011433


## 前書き
事前にVagrantの実行環境が必要です。

## 使い方
### bundleを利用する場合
以下のコマンドを実行しましょう

```sh
bundle install
bundle exec berks vendor cookbooks/
vagrant up
```

### ChefDKを利用する場合
https://downloads.chef.io/chef-dk/

```sh
berks vendor cookbooks/
vagrant up
```


## 仕様
以下のURLにDigitsが立ち上がります。

http://localhost:5000



あと、`docker-compose-file/images`に各データは保存されるようになってます。ここをバックアップしておけば事故らないはず。

## ライセンス
MIT