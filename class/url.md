# URL クラス

URL クラスは、URL を操作するクラスです。

|関数名|
|----|
|public static function create($url, $params = [])|


## public static function create($url, $params = [])

URL を作成します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$url|必須|作成する URL|
|$url|必須|URL に連結するパラメータ値|

### 返り値

string
作成された URL

### 例

```
$url = \core\url::create('test/sample', ['a','b', 'c']);
echo ($url);

$ https://192.168.33.10/test/sample/a/b/c
```
