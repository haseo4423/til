## command(Linux/Mac)

* シンボリックリンク作成 `ln -s XXXX 1903-01`

- 色付きlsのエイリアスコマンド作成
```console
alias ls='ls -FG'
alias ll='ls -laFG'
alias la='ls -laFG'
source ~/.bashrc
```

- PHPを使ってパスワードハッシュを生成
```console
php -r 'echo password_hash("パスワードを入れる", PASSWORD_BCRYPT), PHP_EOL;'
```
