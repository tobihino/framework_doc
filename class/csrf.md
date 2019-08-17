# CSRF クラス

CSRF クラスは、クロスサイトリクエストフォージェリ対策用のトークン発行と、検証を行うクラスです。

|関数名|
|----|
|public static function create()|
|public static function check()|


## public static function create()

クロスサイトリクエストフォージェリ対策用をトークン発行します。

### パラメータ

なし

### 返り値

string
CSRF トークン

### 例

```
csrf::create();
```

## public static function check()

クロスサイトリクエストフォージェリ対策用をトークンを検証します。

### パラメータ

なし

### 返り値

string
CSRF トークン

### 例

```
csrf::check();
```
