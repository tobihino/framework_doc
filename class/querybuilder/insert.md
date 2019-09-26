# INSERT クラス

INSERT クラスは、INSERT SQL の発行や実行を行います。

|関数名|
|----|
|public function __construct($con)|
|public function insert($table)|
|public function field($field, $value, $placeholder=true)|
|public function get_sql()|
|public function execute()|

## 使用例

```
use \core\db;
use \core\querybuilder\insert;

$insert = new insert(new db());
return $insert
    ->insert('data')
    ->field('data_id',      '1')
    ->field('data_name',    'my_name')
    ->field('created_at',   'NOW()', false)
    ->execute();
```

## public function __construct($con)

INSERT クラスのコンストラクトです。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$con||\core\db class を渡します|

### 返り値

$this

## public function insert($table)

INSERT 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$table|必須|INSERT 先のテーブルを指定します。|

### 返り値

$this

## public function field($field, $value, $placeholder=true)

INTO TO 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$field|必須|フィールド名を指定|
|$value|必須|値を指定|
|$placeholder|true|フィールドへの値指定を、プレースホルダーを利用するかどうかを指定<br>true : する,<br>false : しない|

### 返り値

$this

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