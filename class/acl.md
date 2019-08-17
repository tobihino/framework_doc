# ACL クラス

ACL クラスは、認証を管理する機能を提供するクラスです。

|関数名|
|----|
|public static function get_all()|
|public static function has_access($roll_key)|

## public static function get_all()

ログイン中のユーザーに割り当てられているロール情報を一覧で返します。

### パラメータ

なし

### 返り値

array
ログインユーザーに割り当てられている roll_key の一覧

### 例

```
acl::get_all();

出力 :

[0] => full
```




## public static function has_access($roll_key)

ログイン中のユーザーに、引数で指定した roll_key に割り当てられているかどうかを判定して返します。

### パラメーター

|引数|説明|
|----|----|
|$roll_key|割り当てを確認する roll_key を指定|

### 返り値

boolean
ROLL_KEY を割り当てられていたら true 、そうでなければ、false

### 例

```
acl::has_access('ROLL_KEY');
```

