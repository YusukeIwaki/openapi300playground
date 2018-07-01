OpenAPI 3.0 で記述したapidoc.ymlをHerokuでホストする

* dist/index.html
  * ベースは https://github.com/swagger-api/swagger-ui/blob/master/dist/index.html
  * jsとcssはCDNを利用
  * URLは `/swagger.yml` に書き換え
  * ヘッダは削除 (参考: https://github.com/swagger-api/swagger-ui/wiki/FAQ#how-to-hide-topbar )
* [heroku-buildpack-static](https://github.com/heroku/heroku-buildpack-static)利用
  * /swagger.yml のみ、 `apidoc.yml` を指すように変更。

