# cwkeywords

> 显示长尾关键词组合列表

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|type|类型设置|string|`cd`|类型设置 cd(标题+长尾)/bc(词头+标题)/bcd(词头+标题+长尾) 三种模式|
|limit|显示数量|number|||

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
