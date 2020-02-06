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

bashなどのコマンドラインでproxy設定は下記の様にすれば良いかと思いまう。
```bash
export all_proxy=http://192.168.1.99:8080
export http_proxy=http://192.168.1.99:8080
export https_proxy=http://192.168.1.99:8080
export ALL_PROXY=http://192.168.1.99:8080
export HTTP_PROXY=http://192.168.1.99:8080
export HTTPS_PROXY=http://192.168.1.99:8080
export NO_PROXY=localhost,127.0.0.0/8,127.0.1.1
export no_proxy=localhost,127.0.0.0/8,127.0.1.1
```


## 起動

```
docker-compose up
```
※プロセスをdetach（バックグラウンド動作）にする場合は、 `-d` を末尾に追加してください。

## npm の設定

### 恒久的な設定

```
npm set registry http://localhost:4873/
```

### npm install する時に任意設定

```
npm install --registry http://localhost:4873
```
