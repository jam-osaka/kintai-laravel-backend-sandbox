# Laravel Sail について

* [Docs](https://laravel.com/docs/8.x/sail)

Sail は Laravel 公式のローカル開発環境で Docker を使った開発ができるようになっている

また、[新しいプロジェクトを作成](https://laravel.com/docs/8.x/installation#getting-started-on-linux) すると、`sail` は使えるようになっているため、何も気にしなくてOK
```sh
$ curl -s https://laravel.build/example-app | bash
$ cd example-app
$ ./vendor/bin/sail up -d
```

シェルにエイリアスを作成しておくといいかも？

 ```sh
alias sail='vendor/bin/sail'
 ``` 

sail では、デフォルトで docker-compose.yml が用意されていて、Laravel が機能するための Docker コンテナが定義されている  
`laravel.test` サービス？ は、 Laravel を動かすためのメインのサービス？

## Sail を使ってコマンドを実行

Sail を使うことでコンテナ内でコマンドを実行できるため、ローカルコンピュータからは分離した環境でコマンドを実行できる

* バックグラウンドで起動
    ```sh
    $ sail up -d
    ```

* バックグラウンドで起動しているコンテナを停止
 	```sh
    $ sail stop
    ```

* MySQL に接続する
    ```sh
    $ sail mysql
    ```

