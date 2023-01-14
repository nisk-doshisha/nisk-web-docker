# HTTPSでWordpressを簡単に立てるdocker-compose

## 概要
Dockerを使って、WordpressをHTTPSで簡単に構築できるdocker-composeです。

## 事前準備
- docker及びdocker-composeがインストールされている環境（EC2インスタンス等）
- 独自ドメイン（※オプション）
- 22, 80, 443ポートが解放されていること

## やり方
1. どこの場所でも良いので`git clone`で本リポジトリをコピーする
2. `cd nisk-web-docker`
3. `docker-compose up -d`
4. ブラウザ等で環境にアクセスする

とっても簡単！！

## 補足

### 自身のlocal環境でやる場合
.envファイルは次のように設定する
```
PUBLISH_ENV=local
DOMAIN=localhost
```


### ドメインがある環境でやる場合
.envファイルは次のように設定する 

ステージング環境の場合
```
PUBLISH_ENV=staging
DOMAIN=<example>.com
```

本番環境の場合
```
PUBLISH_ENV=production
DOMAIN=<example>.com
```

## 注意
- wordpressのタグはlatestにしてあるのでバージョンが新しくなったら対応が必要かもしれません
- `PUBLISH_ENV=staging`の場合、ブラウザでアクセスした際に警告が出ます

## 参考
- https://qiita.com/kuboon/items/f424b84c718619460c6f
- https://qiita.com/github0013@github/items/71c44d7bf4faf63c1956