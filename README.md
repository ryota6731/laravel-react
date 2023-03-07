<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## laravel-React 環境構築手順

### clone
- **Use this template** からリポジトリを作成する。
- 作成したリポジトリをlocalへcloneする。

### docker
- docker-compose.ymlがある階層で以下を実行する 
・docker/nginxへlogsフォルダを作成
・docker compose up -d
・docker compose ps でコンテナの起動を確認

### composer
- .envファイルを作成し.env.exampleの」内容をコピーし以下画像のように書き換える  
![スクリーンショット 2023-03-07 12 38 24](https://user-images.githubusercontent.com/96375170/223314710-e0f52e3b-f885-4fd9-8178-86ab89b2759c.png)

- docker compose exec -it shb-v2-app bash　コンテナに入る
- chmod -R guo+w storage
- composer install

### laravel初期設定
- php artisan key:generate
- php artisan migrate
- composer dump-autoload

### npm install
- npm install
- npm run dev　Laravelの初期画面が表示されるか確認
- http://localhostへアクセスし同じ画面が表示されるか確認

## 開発する際、dockerを立ち上げた時は、毎回以下を実行する必要があります。
- composer install
- npm install
