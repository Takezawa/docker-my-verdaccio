# verdaccio

プライベートな npm リポジトリ

## 公式サイト

https://verdaccio.org/en/

## 既存のアカウント

Username: jpicado Password: jpicado

## proxyサーバがある環境の場合

`conf/config.yaml` の20行目にあるproxyの設定をしてください。
例：ip:192.168.1.99 port:8080 なproxyサーバーの場合
```
# if use proxy server
http_proxy: http://192.168.1.99:8080/
https_proxy: http://192.168.1.99:8080/
no_proxy: localhost, 127.0.0.1
```

## 起動

```
docker-compose up
```
※プロセスをdetach（バックグラウンド動作）にする場合は、 `-d` を末尾に追加してください。
※２回目以降の起動は、upをstartに変更してください。

## npm の設定

### 恒久的な設定

```
npm set registry http://localhost:4873/
```

### npm install する時に任意設定

```
npm install --registry http://localhost:4873
```
