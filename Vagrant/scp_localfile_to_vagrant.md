# vagrant内にファイルを転送する

```terminal
★ファイルの転送先にしたいvagrantディレクトリにいるか確認 && 仮想マシンの名前を確認
$ vagrant status
★vagrantのssh設定をファイルに書き出す
$ vagrant ssh-config > ssh.config
★ファイル転送 @の後を仮想マシンの名前に変える
$ scp -F ssh.config hello.txt vagrant@default:~/
★ログイン
$ vagrant ssh
★権限変更
$ sudo su -
★ファイルが転送されたか確認
$ find / -name hello\*
```
