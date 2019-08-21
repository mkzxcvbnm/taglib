# nav

> 导航

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|typeid|类型|number|`必填`|`1`-主导航 `2`-尾导航 `3`-全部|
|limit|显示数量|number|`10`|&nbsp;|

**字段**

|别名|调用代码|
|:--:|:--:|
|导航名称|{$nav.title}|
|导航副标题|{$nav.subtitle}|
|导航封面图|{$nav.pic}|
|导航链接|{$nav.url}|
|导航子栏目|{$nav.child}|

{% sample lang="php" %}
**例子**

```html
<yunu:nav typeid="1" limit="20">
<li>
    <a href="{$nav.url}">{$nav.title}</a>
    <volist name="nav['child']" id="v">
    <ul>
        <li><a href="{$v.url}">{$v.title}</a></li>
    </ul>
    </volist>
</li>
</yunu:nav>
```

例子参数含义

>`cid="1"`显示"导航栏显示"为"主导航"或"都显示"的栏目

>`limit="20"`显示20条信息

{% endmethod %}
