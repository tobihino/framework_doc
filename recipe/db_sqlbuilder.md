## SELECT / INSERT / UPDATAE / DELETE の SQL を発行できます。

## JOIN 句の書き方

```
$select = new \core\select(new \core\db());
$rs = $select
    ->select('tbl_1.value')
    ->from('tbl_1 JOIN tbl_2 ON tbl_1.id = tbl_2.id')
    ->where('tbl_1.id = ?', 1)
    ->fetch_all();
```
