## フィールドとフィールドセットの関係

### フィールドセットの作り方

```
$myfieldset = new \core\fieldset()
//
$myfieldset->append('id',       ['label' => '主キー']);
$myfieldset->append('value',    ['label' => '値']);
```

### フィールド値の取得方法

```
$myfieldset = new \core\fieldset()
//
$myfieldset->append('id',       ['label' => '主キー']);
$myfieldset->append('value',    ['label' => '値']);
//
$id = $myfieldset->get_value('id');
$value = $myfieldset->get_value('value');
```

### フィールド値の設定方法

```
$myfieldset = new \core\fieldset()
//
$myfieldset->append('id',       ['label' => '主キー']);
$myfieldset->append('value',    ['label' => '値']);
//
$myfieldset->set_value('id', 6);
$myfieldset->set_value('value', '情けは人のためならず');
```

### $_POST からの入力値を取得する

```
$myfieldset = new \core\fieldset()
//
$myfieldset->append('id',       ['label' => '主キー']);
$myfieldset->append('value',    ['label' => '値']);
//
$myfieldset->psot();
```
```$_POST['id']``` と、```$_POST['value']``` の内容がフィールドに値として設定されます。

### バリデーションの実行

```
$myfieldset = new \core\fieldset()
//
$myfieldset->append('id',       ['label' => '主キー']);
$myfieldset->append('value',    ['label' => '値']);
//
$myfieldset->validate('required', 'id');
$myfieldset->validate('required', 'value');
//
if ($myfieldset->is_valid == true)
{
    echo('成功');
}
else
{
    echo('成失敗');
}
```

```validete``` メソッドは、即時実行され、実行結果は、is_valid に設定されます。


### オリジナルのバリデーション実行

オリジナルのバリデーションを実行したい場合は、します。

```
$myfieldset = new \core\fieldset()
//
$myfieldset->append('id',       ['label' => '主キー']);
$myfieldset->append('value',    ['label' => '値']);
//
if ($myfieldset->get_value('id')=='')
{
    $myfieldset->set_field_error('id', '主キーは必ず指定してください。');
}
if ($myfieldset->get_value('value')=='')
{
    $myfieldset->set_field_error('value', '値は必ず指定してください。');
}
//
if ($myfieldset->is_valid == true)
{
    echo('成功');
}
else
{
    echo('成失敗');
}
```

