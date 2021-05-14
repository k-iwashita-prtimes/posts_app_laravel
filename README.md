# laravel_enviroment



## get started


#### クローンする
```
$ git clone https://github.com/k-iwashita-prtimes/posts_app.git
```

#### cloneしたディレクト配下へcdした後、dockerをbuild, upする。
```
$ doker compse build
$ docker compose up -d 
```

#### dockerコンテナの中で、必要なファイルの生成を行う
```
$ docker compose exec app bash
$ composer install
$ cp .env.example .env
$ php artisan key:generate
$ exit 
```

#### http://127.0.0.1:10080/  へ接続する。


#### ※MySQLに接続したい
```
$ docker-compose exec db bash -c 'mysql -u${MYSQL_USER} -p${MYSQL_PASSWORD} ${MYSQL_DATABASE}'
```


