## 動作モードの設定

動作モードとは、TOBIHINO FRAMEWORK が、動作しているモードを指定するものです。

## 指定する方法

```/site/config/application.md``` 内に記述します。

```
<?php
return
[
    'APP_MODE'      => APP_MODE_DEVELOPMENT,　 // ここで指定
];
```