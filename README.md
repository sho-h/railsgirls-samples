# railsgirls-samples

これはRailsGirlsのガイドに沿って作成したRailsアプリケーションのサンプル
です。masterブランチには何もありません。

[/heroku](http://railsgirls.jp/heroku/)のような一部のガイドでも正しく動
作するために、ガイドごとにブランチを作成しています(折角なので今後も使え
るようにブランチ名は"<開催日>/<開催地>/<ガイド>"としています)。

clone後それぞれのブランチに切り替えるか直接ブランチの内容をダウンロード
して使ってください。

* /installまで: [20151114/matsue/install](https://github.com/sho-h/railsgirls-samples/archive/20151114/matsue/install.zip)
* /appまで: [20151114/matsue/app](https://github.com/sho-h/railsgirls-samples/archive/20151114/matsue/app.zip)
* /app→/herokuまで: [20151114/matsue/app2heroku](https://github.com/sho-h/railsgirls-samples/archive/20151114/matsue/app2heroku.zip)
* /app→/mogokまで: [20151114/matsue/mogok](https://github.com/sho-h/railsgirls-samples/archive/20151114/matsue/app2mogok.zip)

展開後にまだconfig/secrets.ymlを作成していない場合は以下のコマンドで作
成してあとはガイドに従ってください。

```
$ ruby -r yaml -e "puts({"development": {"secret_key_base": '`rake secret`'}, "test": {"secret_key_base": '`rake secret`'}, "production": {"secret_key_base": '<%= ENV["SECRET_KEY_BASE"] %>'}}.to_yaml)" > config/secrets.yml
```
