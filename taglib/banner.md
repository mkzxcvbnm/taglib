# banner

> 幻灯片

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|type|类型|number|`0`|`0`-全部 `1`-PC `2`-手机|
|orderby|排序|string|`id desc`|`asc`-正序 `desc`-倒序|
|limit|显示数量|number|`10`||

**字段**

|字段名|别名|
|:----:|:--:|
|{$flink.id}|ID|
|{$flink.title}|幻灯片名称|
|{$flink.pic}|主图片|
|{$flink.fpic}|副图片|
|{$flink.url}|链接|
|{$flink.sort}|排序|
|{$flink.type}|类型|

{% sample lang="php" %}
**例子**

```html
<yhcms:banner type="1" limit="10" orderby="sort desc">
  <li>
    <a href="{$banner.url}"><img src="{$banner.pic}" alt="{$banner.title}"></a>
  </li>
</yhcms:banner>
```

例子参数含义

>`type="1"`类型为"PC"

>`limit="10"`显示10条信息

>`orderby="sort desc"`按照sort(排序字段)的倒序

{% endmethod %}
