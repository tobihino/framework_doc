## define 設定

アプリケーション内で利用されている定数の一覧です。定数は、```/core/config/application.php``` で定義されます。上書きする場合は、```/app/config/application.php``` または、 ```/site/config/application.php``` を更新ください。設定自体は、/public/index.php から呼び出されて実行されています。


### /public/index.php

|キー|説明|例|
|----|----|----|
|FRAMEWORK_PREFIX|-|tobihino|
|APP_DIR|アプリケーションのルートディレクトリ|/var/www/apps/appdir|
|APP_MODE_DEVELOPMENT|動作モード定義（開発）|development|
|APP_MODE_STAGING|動作モード定義（ステージング）|staging|
|APP_MODE_PRODUCTION|動作モード定義（本番）|production|

### /config/application.php

|キー|説明|例|
|----|----|----|
|APP_NAME|アプリケーションの名前|MyApplication|
|APP_KEY|アプリケーションを識別するキー|-|
|APP_MODE|動作モード<br>APP_MODE_DEVELOPMENT<br>APP_MODE_STAGING<br>APP_MODE_PRODUCTION<br>が指定可能|-|-|
|APP_DEBUG|デバッグモードを指定<br>0 : 無効<br>1 : 有効|1|
|APP_FRAMWROK_DIR|フレームワークのルートディレクトリ|/var/www/apps/appdir/tobihino|
|APP_CACHE_DIR|キャッシュのルートディレクトリ|/var/www/apps/appdir/tobihino/cache|
|APP_FILE_DIR|ファイルのルートディレクトリ|/var/www/apps/appdir/tobihino/file|
|APP_VIEW_DIR|ファイルのルートディレクトリ|/var/www/apps/appdir/tobihino/view|
|APP_BASE|サーバー上の設置位置<br>例  ```/appdir```|-|
|APP_HOST|http://192.168.33.10/appdir|-|
