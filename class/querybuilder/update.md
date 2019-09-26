# UPDATE クラス

UDPATE クラスは、UDPATE SQL の発行や実行を行います。

|関数名|
|----|
|public function __construct($con)|
|public function update($table)|
|public function set($field, $value, $placeholder = true)|
|public function where($where, ...$params)|
|public function get_sql()|
|public function execute()|

## 使用例

```
use \core\db;
use \core\querybuilder\update;

$update = new update(new db());
$update
    ->update('data')
    ->set('data_name',          'my_name')
    ->set('updated_at',         'NOW()', false)
    ->where('data_id = ?',      1)
    ->execute();
return true;

```

## public function __construct($con)

UDPATE クラスのコンストラクトです。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$con||\core\db class を渡します|

### 返り値

$this

## public function insert($table)

UDPATE 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$table|必須|UPDATE 先のテーブルを指定します。|

### 返り値

$this

## public function set($field, $value, $placeholder = true)

SET 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$field|必須|フィールド名を指定|
|$value|必須|値を指定|
|$placeholder|true|フィールドへの値指定を、プレースホルダーを利用するかどうかを指定<br>true : する,<br>false : しない|

### 返り値

$this

## public function where($where, ...$params)

WHERE 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$where|必須|where 句をプレースホルダー付きで記載して渡します。|
|$params|必須|プレースホルダーの中身を指定します。|

## public function get_sql()

SQL を返します

### パラメータ

なし

### 返り値

string:
SQL


## public function execute()

SQL を実行します。

### パラメータ

なし

### 返り値

\core\db->query の実行結果