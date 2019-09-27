## データベースへの接続

MySQL データベースへの接続を基本として、データベース操作をする場合のレシピです。

### データベースへの接続情報を config\db.php に、記述します。

```
<?php
return
[
    'default' =>
    [
        'dsn'   => 'mysql:host=localhost;dbname=mydb;charset=utf8',
        'user'  => 'root',
        'pass'  => 'root',
    ],
];
```

複数のDBに接続したい場合は、以下のように、それぞれの DB への接続情報を記述します。

```
<?php
return
[
    'default' =>
    [
        'dsn'   => 'mysql:host=localhost;dbname=mydb;charset=utf8',
        'user'  => 'root',
        'pass'  => 'root',
    ],
    'db2' =>
    [
        'dsn'   => 'mysql:host=localhost;dbname=mydb2;charset=utf8',
        'user'  => 'root',
        'pass'  => 'root',
    ],
];
```

### データベースへの接続

接続情報の ```default``` に接続する場合は、以下のように記述します。

```
$db = new \core\db();

```

```db2``` を指定したい場合は、以下のように記述します。

```
$db = new \core\db('db2');

```

### SQL の発行方法

#### SQL の実行

SQL を発行するには、DB に接続後、SQL と パラメーターを query メソッドに渡します。

```
$con = new \core\db();
$sql = 'DELETE FROM TBL WHERE ID=:ID;';
$sql_params = [':ID'=1];
$rst = $con->query($sql, $sql_params);
```

#### SQL の実行結果を配列で受取

SELECT の結果を、配列で受取たい場合などは、fetcg_all メソッドを利用します。

```
$con = new \core\db();
$sql = 'SELECT * FROM TBL WHERE ID=:ID;';
$sql_params = [':ID'=1];
$rst = $con->fetch_all($sql, $sql_params);
```





