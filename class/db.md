# DB クラス

DB クラスは、データベースへの接続、SQL の発行と実行結果の取得を行うクラスです。

|関数名|
|----|
|public function current_connection()|
|public function query($sql, $param = [])|
|public function fetch_all($sql, $params = [])|

## public function __construct()

クラスのインスタンスを作成した時点で、環境設定ファイル db に従って、MySQL に接続する。接続後、query メソッドを利用して、DB を操作します。 

### パラメータ

なし

### 返り値

object - 接続情

### 例

```
$con = new \core\db();
```
## public function current_connection()

既定の接続を返します。

### パラメータ

なし

### 返り値

object - 既定の接続

### 例

```
$obj = new \core\db();
$con = $obj->current_connection();
```

## public function query($sql, $param = [])

既定の接続を利用して、SQL に、パラメータを渡して実行します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$sql|必須|実行する SQL を指定します。|
|$param|[]|必要に応じて、SQL の実行に必要なパラメータを指定します。|

### 返り値

array
結果の行を含む連想配列あるいは数値添字配列の配列を返します。

### 例

```
$con = new \core\db();
$sql = 'DELETE FROM TBL WHERE ID=:ID;';
$sql_params = [':ID'=1];
$rst = $con->query($sql, $sql_params);
```

## public function fetch_all($sql, $param = [])

既定の接続を利用して、SQL に、パラメータを渡して実行して結果を取得します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$sql|必須|実行する SQL を指定します。|
|$param|[]|必要に応じて、SQL の実行に必要なパラメータを指定します。|

### 返り値

array
結果の行を含む連想配列あるいは数値添字配列の配列を返します。

### 例

```
$con = new \core\db();
$sql = 'SELECT * FROM TBL WHERE ID=:ID;';
$sql_params = [':ID'=1];
$rst = $con->fetch_all($sql, $sql_params);
```
