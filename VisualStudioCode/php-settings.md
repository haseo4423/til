## phpcsの設定

- `brew install php-code-sniffer`
- `brew install composer`
- `composer global require squizlabs/php_codesniffer`

##### vscode settings編集

- `"phpcs.standard": "PSR2"`

##### コマンドで確認したい場合

- `./vendor/bin/phpcs --standard=phpcs.xml .`

## PHP Debugの設定

##### サーバー側にxdebugがインストールされていること
- 自分のvagrantリポジトリはインストール済み

##### ローカルのPHPをv7.x以上に更新する
- `php -v`でバージョン確認

##### vscodeデバッグのlaunch.jsonに追記

```json
{
  "name": "Listen for XDebug",
  "type": "php",
  "request": "launch",
  "port": 9002,
  "serverSourceRoot": "/var/www/html", ★サーバー側のドキュメントルートに変える
  "localSourceRoot": "${workspaceRoot}"
}
```

## php cs fixerの設定

##### php-cs-fixerをインストールしておく

- `brew install php-cs-fixer`
