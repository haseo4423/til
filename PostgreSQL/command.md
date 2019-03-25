### PostgreSQLコマンド

- `CREATE ROLE username WITH LOGIN PASSWORD 'password';`
  - ユーザー作成

- `CREATE DATABASE databasename;`
  - データベース作成

- `GRANT ALL PRIVILEGES ON DATABASE databasename TO username;`
  - ユーザーにDB権限を付与

- `psql -h hostname -U username -d databasename`
  - ログイン

- `TRUNCATE TABLE table_name RESTART IDENTITY;`
  - テーブルを空にしてindexも振り直す
