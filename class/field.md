# Field クラス

Field クラスは、Fieldset クラスで利用する、Field オブジェクトを宣言するクラスです。

|関数名|
|----|
|public function __construct($name, $property=[])|
|public function set_error($error_message)|
|public function set_property($name, $value)|
|public function get_property($name)|
|public function to_array()|
|public function post($prefix='')|

## public function __construct($name, $property=[])

コンストラクト。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$name|必須|フィールド名を指定します。|
|$property|[]|フィールドに属するプロパティを指定します。|

### 返り値

なし

## set_error($error_message)

フィールドにエラーを設定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$error_message|必須|エラーメッセージを指定します。|

### 返り値

なし

