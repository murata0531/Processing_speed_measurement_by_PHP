# Processing_speed_measurement_by_PHP

PHPで処理速度を測るリポジトリ

単純な計算やデータベースアクセスの速度を測る

環境

Laravel



コンテナ作成

```
$ docker-compose up -d --build
```

コンテナとイメージ破棄

```
$ docker-compose down --rmi all --volumes --remove-orphans
```

各種コンテナに入る

```
appコンテナ：ここでlaravelやphpなどを動かしている
$ docker-compose exec app bash
```

```
dbコンテナ：ここでmysqlを動かしている
$ docker-compose exec db bash
```

```
webコンテナ：ここでnginxを動かしている
$ docker-compose exec web bash
```

構築

```
$ docker-compose exec app bash
```

```
bash# cp .env.example .env
```

```
bash# composer install

bash# php artisan key:generate

```

# 注意

.envファイルの ` DB_HOST ` の項目は ` db ` にする

mysqlのユーザやパスワードは ` mysql/Dockerfile ` に記述してある