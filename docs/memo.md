## プロジェクトの作成

```sh
$ curl -s "https://laravel.build/kintai-laravel-backend" | bash
$ cd kintai-laravel-backend
$ git init .
$ git add .
$ git commit -m "init"
$ git remote add origin https://jam-osaka@github.com/jam-osaka/kintai-laravel-backend-sandbox.git
$ git branch -M main
$ git push -u origin main
```

## プロジェクトの設定

### 環境の設定

`.env` で環境の設定を行う

```.env
# ポートの設定
APP_PORT=8000

# DB の名前
DB_DATABASE=kintai_app
```

### Laravel のアプリの設定

Laravel の設定は、`config/app.php` で行う

```.env
// タイムゾーンの設定
'timezone' => 'Asia/Tokyo',

// 言語の設定
'locale' => 'ja',
```


## /api/hello に対応するルートを定義

`routes/api.php` に以下を追加する

```api.php
Route::get('/hello', function () {
    return 'hello world';
});
```

## 起動

```sh
$ ./vendor/bin/sail up -d
```

## アクセスしてみる

http://localhost:8000/api/hello にアクセスすると、 `hello world` が表示される

