- getpocket.comで「CreateNewApp」からアプリ作成
- 認証コードを取得するAPI実行
```
Example request (JSON):

POST https://getpocket.com/v3/oauth/request HTTP/1.1
Host: getpocket.com
Content-Type: application/json; charset=UTF-8
X-Accept: application/json

{"consumer_key":"1234-abcd1234abcd1234abcd1234",
"redirect_uri":"pocketapp1234:authorizationFinished"}
```
```
Example response (JSON):

HTTP/1.1 200 OK
Content-Type: application/json
Status: 200 OK

{"code":"dcba4321-dcba-4321-dcba-4321dc"}
```
- ブラウザ上でアカウント利用を承認するURLにアクセス
```
https://getpocket.com/auth/authorize?request_token=dcba4321-dcba-4321-dcba-4321dc&redirect_uri=test
```
- アクセストークンを取得するAPI実行
```
Example request (JSON):

POST /v3/oauth/authorize HTTP/1.1
Host: getpocket.com
Content-Type: application/json; charset=UTF-8
X-Accept: application/json

{"consumer_key":"1234-abcd1234abcd1234abcd1234",
"code":"dcba4321-dcba-4321-dcba-4321dc"}
```
```
Example response (JSON):

HTTP/1.1 200 OK
Content-Type: application/json
Status: 200 OK

{"access_token":"5678defg-5678-defg-5678-defg56",
"username":"pocketuser"}
```
