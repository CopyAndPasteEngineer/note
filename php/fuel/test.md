# FeulPHP自動テスト導入

## docker起動

```
docker-compose up -d --build apache2 mysql phpmyadmin redis selenium
```

## docker停止

```
docker-compose down
```



## ワークスペースログイン
```
docker exec -it laradock_workspace_1 bash
```

## Dokerの削除
```
docker rm $(docker ps -q -a)
```

## テストライブラリの導入
```
composer require phpunit/phpunit
composer require php-webdriver/webdriver
```

https://phpunit.readthedocs.io/ja/latest/<br>
https://github.com/php-webdriver/php-webdriver<br>

## テストの実行
```
# テスト
php oil test

# テストスイーツの指定
php oil test --group=App

# デバック出力許可
php oil test --debug  --group=App
```

ログは`fuel\app\logs\test\coverage`に出ます。

## 参考URL
[FuelPHP でユニットテスト + カバレッジ取得](https://qiita.com/hira3/items/f14bbc64b6a01d575e57)<br>
[FuelPHPにPHPUnitを導入したが、エラーが発生してテストできない](https://qiita.com/Prof/items/eccc8a99b7eb982de817)<br>
[PHP + phpunit + php-webdriver + docker-selenium でブラウザテスト　①環境構築](https://qiita.com/haruna-nagayoshi/items/3ab58005a6ab74309a8f)<br>
[PHP + phpunit + php-webdriver + docker-selenium でブラウザテスト　②テスト実行、エラー対策](https://qiita.com/haruna-nagayoshi/items/bcf61a3e161f3ee10d83)<br>
[Laradockでの環境構築からSeleniumでお手軽スクレイピング](https://qiita.com/heimax/items/6103ee38dc6218d2caa5)
