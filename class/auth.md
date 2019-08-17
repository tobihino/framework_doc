# Auth クラス

Auth クラスは、ユーザーのログイン状態を管理するための機能を提供するクラスです。

|関数名|
|----|
|public static function validate_user($username, $password)|
|public static function login($username, $password)|
|public static function is_login()|
|public static function get_user_id()|
|public static function logout()|

## public static function validate_user($username, $password)

ユーザー名とパスワードの組み合わせが正しいか検証して、結果を返します。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$username|必須|ログインに利用するユーザー名を指定します。|
|$password|必須|ログインに利用するパスワードを指定します。|

### 返り値

boolean
ユーザー名と、パスワードの組み合わせが正しい場合は true を、正しくない場合は、falase を返します。

### 例

```
auth::validate_user('MyName', 'MyPass');
```




## public static function login($username, $password)

ユーザー名とパスワードを指定してログインします。

### パラメータ

|引数|デフォルト|説明|
|----|----|----|
|$username|必須|ログインに利用するユーザー名を指定します。|
|$password|必須|ログインに利用するパスワードを指定します。|

### 返り値

boolean
ログインに成功した場合は true を返します。ログインに失敗した場合は false を返します。

### 例

```
auth::login('MyName', 'MyPass');
```




## public static function is_login()

ログイン中のユーザーを、ログアウトさせます。

### パラメータ

なし

### 返り値

boolean
ログイン中の場合は true を返します。そうでない場合は false を返します。

### 例

```
auth::is_login();
```




## public static function get_user_id()

ログイン中のユーザーの、user_id を取得します。

### パラメータ

なし

### 返り値

int / boolean
ログイン中の場合は、ログインしているユーザーの user_id を返します。ログインしていない場合は false を返します。

### 例

```
auth::get_user_id();
```



## public static function logout()

ログイン中のユーザーを、ログアウトさせます。

### パラメータ

なし

### 返り値

bool
true を返します。

### 例

```
auth::logout();
```
