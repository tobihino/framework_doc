## twig の function / twig を拡張する方法

config フォルダに、twig.php に設定を記載。

### filter の書き方

```
{% filter cs_markdown({template:'default', id:'abc'}) %}
sample text
{% endfilter%}
```
