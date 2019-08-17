# Config クラス

Config クラスは、アプリケーションが動作するために必要な、設定情報を読み込みむクラスです。

|関数名|
|----|
|public static function read($config_name)|

## public static function read($config_name)

config フォルダ内の指定ファイルを順次読み込み、マージした結果を返します。指定ファイルが存在しない場合は、読み込みをスキップします。

[読込の優先順はこちらを参照](../basic/file)

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$config|必須|config ファイルの名前を指定します。|

### 返り値

array

### 例

```
config::read('CONFIG_NAME');
```
