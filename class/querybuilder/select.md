# SELECT クラス

SELECT クラスは、SELECT SQL の発行や実行を行います。

|関数名|
|----|
|public function __construct($con)|
|public function select(...$fields)|
|public function from($table)|
|public function where($where, ...$params)|
|public function order(...$order)|
|public function limit($limit)|
|public function offset($offset)|
|public function get_sql()|
|public function fetch_all()|

## 使用例

```
use \core\db;
use \core\querybuilder\select;

$select = new select(new db());
$rs = $select
    ->select
        (
            'data_id',
            'data_name'
        )
    ->from('data')
    ->where('data_id = ?', 1)
    ->fetch_all();
```

## public function __construct($con)

SELECT クラスのコンストラクトです。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$con||\core\db class を渡します|

### 返り値

$this

## public function select(...$fields)

SELECT 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$fields|必須|SELECT 句を指定します。|

### 返り値

$this

## public function from($table)

FROM 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$table|必須|FROM 句を指定します。|

### 返り値

$this

## public function where($where, ...$params)

WHERE 句を指定します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$where|必須|WHERE 句をプレースホルダー付きで記載して渡します。|
|$params|必須|プレースホルダーの中身を指定します。|

## public function order(...$order)

ORDER 句を指定します。

|引数|デフォルト|説明|
|----|----|----|
|$order|必須|ORDER 句を記載して渡します。|

## public function limit($limit)

LIMIT 句を指定します。

|引数|デフォルト|説明|
|----|----|----|
|$limit|必須|LIMIT 句を記載して渡します。|

## public function offset($offset)

LIMIT 句の OFFSET を指定します。

|引数|デフォルト|説明|
|----|----|----|
|$limit|必須|LIMIT 句の OFFSET を記載して渡します。|

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