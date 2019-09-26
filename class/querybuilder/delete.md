# INSERT クラス

DELETE クラスは、DELETE SQL の発行や実行を行います。

|関数名|
|----|
|public function __construct($con)|
|public function from($table)|
|public function where($where, ...$params)|
|public function get_sql()|
|public function execute()|

## 使用例

```
use \core\db;
use \core\querybuilder\delete;

$delete = new delete(new db());
$delete
    ->from('data')
    ->where('data_id = ?', 1)
    ->execute();
```

## public function __construct($con)

DELETE クラスのコンストラクトです。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$con||\core\db class を渡します|

### 返り値

$this

## public function insert($table)

DELETE 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$table|必須|DELETE 先のテーブルを指定します。|
### 返り値

$this

## public function where($where, ...$params)

WHERE 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$where|必須|where 句をプレースホルダー付きで記載して渡します。|
|$params|必須|プレースホルダーの中身を指定します。|

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