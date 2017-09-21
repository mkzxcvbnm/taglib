# cwkeywords

> 显示长尾关键词组合列表

{% method %}
**参数**
*无*

**字段**

|字段名|别名|
|:----:|:--:|
|{$cwkeywords.name}|名称|
|{$cwkeywords.url}|链接|

{% sample lang="php" %}
**例子**

```html
<yunu:cwkeywords>
    <a href="{$cwkeywords.url}">{$cwkeywords.name}</a>&nbsp;&nbsp;&nbsp;&nbsp;
</yunu:cwkeywords>
```

{% endmethod %}
