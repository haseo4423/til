## プライベートCA構築

```terminal
$ openssl req -new -x509 -newkey rsa:2048 \
  -out sample-dev.cacrt.pem -keyout sample-dev.cakey.pem \
  -subj "/C=JP/ST=Tokyo/L=Nerimaku/O=ExampleCompany/OU=ExampleCertificateAutholity/CN=sample-local5.dev.jp"
Generating a 2048 bit RSA private key
...................................................................+++
...........................................+++
writing new private key to 'sample-dev.cakey.pem'
Enter PEM pass phrase: ★sample0077
Verifying - Enter PEM pass phrase: ★sample0077
-----
```

##### 秘密鍵複合
```teminal
openssl rsa -in sample-dev.cakey.pem -out sample-dev.canokey.pem
Enter pass phrase for sample-dev.cakey.pem: ★sample0077
writing RSA key
```
