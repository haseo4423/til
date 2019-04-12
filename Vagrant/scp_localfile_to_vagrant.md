# vagrant内にファイルを転送する

```terminal
$ vagrant status
$ vagrant ssh-config > ssh.config
$ scp -F ssh.config hello.txt vagrant@default:~/
$ vagrant ssh
$ sudo su -
$ find / -name hello\*
```
