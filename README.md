# README

## プロジェクト名を変更

プロジェクトの全ファイルを`app_name`でグレップし、任意のプロジェクト名で置換してください。

## .envファイル作成

`.env.sample`をコピーして`.env`ファイルを作成してください。

```bash
$ cp .env.sample .env
```

.envファイルの下記環境変数の値を設定してください。

- `MYSQL_DATABASE`

- `MYSQL_ROOT_USER`

- `MYSQL_ROOT_PASSWORD`

## Docker起動

```bash
$ docker-compose build
$ docker-compose up
```

## DB作成

```bash
$ docker-compose exec app rails db:create
```

## Dockerfileやdocker-compose.ymlの変更を反映

```bash
$ docker-compose up --build
```

## ローカルからMySQLコンテナに接続

```bash
$ mysql -u root -p -h localhost -P 3306 --protocol=tcp
```

## 参照

[Rails5+Mysql on Docker: Qiita](https://qiita.com/azul915/items/5b7063cbc80192343fc0)
