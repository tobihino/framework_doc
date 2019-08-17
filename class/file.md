# File クラス

File クラスは、ファイル操作を行うための機能を提供します。操作する場所は、定数 ```APP_FRAMEWORK_DIR``` で指定されたフォルダ以下の場所に限定されます。

|関数名|
|----|
|public static function get_list($path='', $ext='', $recursion=true)|
|public static function path_join(...$path)|
|public static function mkdir($path)|

## public static function get_list($path='')

ファイルの一覧を取得します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$path|''|指定したフォルダ以下のファイルの一覧を取得します。|
|$ext|''|取得したいファイルの拡張子を指定します。|
|$recursion|true|再帰して下層フォルダ内のファイルを一覧に取得するかどうかを指定します。|

### 返り値

array
ファイルの一覧を返します。

### 例

```
$rs = \core\get_list();
```




## public static function path_join(...$path)

指定した複数の文字列をパス形式に整形しながら連結します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$path|[]|連結したいパスを渡します。|

### 返り値

string
連結したパス文字列

### 例

```
$var = \core\path_join('dir1', 'dir2');
var_dump($var);
```




## public static function mkdir($path)

指定したフォルダを作成します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$path|必須|作成したいフォルダを指定します。|

### 返り値

boolean
成功したら true 失敗したら false を返します。

### 例

```
$var = \core\mkdir('file/dir1/dir2');
```

