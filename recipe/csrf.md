## CSRF (クロスサイトリクエストフォージェリ) 対策の方法

CSRF (クロスサイトリクエストフォージェリ) 対策するためのレシピです。

入力画面、完了画面という２つの画面があり、完了画面で POST で送信されたデータを、データベースに登録する仕組みを作成した場合に、CSRF 対策が取られていない場合、特に対策がないと、データベースに攻撃者が任意のデータを好きなだけ登録できてしまいます。
そこで、データ送信されてきたときに、送信元が正しいことを確認して確認できるようにします。


### 送信元コード

entry.twig (入力画面)

CSRF トークンを出力するコードを書いておきます。

```<input type="hidden" name="csrf_token" value="{{ csrf_token() }}">```

```
<form action="update" method="post">
<input type="text" name="data1" value="">
<input type="submit" value="送信">
<input type="hidden" name="csrf_token" value="{{ csrf_token() }}">
</form>
```

### 受信先コード

update.php (完了画面)

入力画面から送信された CSRF トークンが正しいかどうかを判断して、正しくない場合処理を中断します。

```
namespace app\controller\sample;

use \core\csrf;
use \core\response;

class myclass
{
    public function action_update($params)
    {
        if (!csrf::check())
        {
            response::redirect(url::create('/404'));
        }
    }
}
```
