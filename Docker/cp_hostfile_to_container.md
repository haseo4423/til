# ホストからコンテナにファイルを転送する

```terminal
★コンテナIDを確認する
$ docker ps
★確認したコンテナIDで置き換えて転送を実行する
$ docker cp hello.txt {コンテナID}:/etc/hello.txt
```
