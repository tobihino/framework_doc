# FieldSet クラス

Fieldset クラスは、Field クラスを取りまとめて、一括して操作する機能を提供するクラスです。

|関数名|
|----|
|public function append($name, $property=[])|
|public function post($prefix='')|
|public function get_field($name)|
|public function set_value($name, $value)|
|public function set_values($values)|
|public function get_values()|
|public function to_array()|
|public function get_error_messages()|
|public function get_fs_error_messages()|
|public function set_error($name, $error_message)|
|public function set_fs_error($error_message)|
|public function validate(...$args)|

## public function append($name, $property=[])

フィールドセットにフィールドを追加します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$name|必須|追加するフィールドの名前|
|$property|必須|追加するフィールドに設定するプロパティ値|

### 返り値

なし

### 例

```
```




## public function post($prefix='')

Fieldset に登録されている Field の名前と、$_POST の変数名と突き合わせて、FIeld に値を登録します。$prefix を指定することで、$_POST の変数名の先頭に、$prefix で指定した文字列を付けたものと、Field の名前を突き合わせるようになります。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$prefix|''|$_POST から値を取得するときに、$prefix を指定する場合に付けます。|

### 返り値

なし

### 例

```
```




## public function get_field($name)

指定した名前の Field オブジェクトを取得します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$name|必須|取得したい Field オブジェクトを指定します。|

### 返り値

object
field オブジェクトが戻されます。

### 例

```
```




## public function set_value($name, $value)

指定した名前の Field オブジェクトに値を登録します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$name|必須|値を登録したい Field の名前を指定します。|
|$value|必須|登録したい値をを指定します。|

### 返り値

なし

### 例

```
```




## public function get_value($name)

指定した名前の Filed オブジェクトに登録されている値を取得します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$name|必須|値を取得したい Field の名前を指定します。|

### 返り値

variant
Field オブジェクトに登録されている値が戻されます。

### 例

```
```




## public function set_values($$values)

指定した名前の Field オブジェクトに値を、まとめて登録します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$values|必須|値を登録したい Field の名前と値の組み合わせを指定します。|

### 返り値

なし

### 例

```
```




## public function get_values()

Filedset オブジェクトに登録されている、すべての Field の値を取得します。

### パラメータ

なし

### 返り値

array
Field オブジェクトに登録されているすべての値が戻されます。

### 例

```
```




## public function to_array()

登録されている、すべての情報を配列で返します。

### パラメータ

なし

### 返り値

### 例

```
```



## public function set_field_error()

Fieldset に登録されている Field にエラー登録します。Fieldset の IsValid 変数は、false に設定されます。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
||||

### 返り値

### 例

```
```




## public function get_field_error_messages()

Fieldset に登録されている Field のエラーを、すべて取得します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
||||

### 返り値

### 例

```
```





## public function get_error($error_message)

Fieldset のエラーを取得します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
||||

### 返り値

### 例

```
```




## public function set_error($error_message)

Fieldset にエラーを登録します。Fieldset の IsValid 変数は、false に設定されます。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
||||

### 返り値

### 例

```
```




## public function validate($validator, ...$args)

Fieldset オブジェクトに登録されている Field オブジェクトがもつ、Validate を実行します。検証に失敗した場合は、Fieldset の IsValid 変数は、false に設定されます。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$validator|必須|実行する Validator を指定します。|
|$..args||Validator ごとに必要とする値を指定します。|

### 返り値

### 例

```
```


