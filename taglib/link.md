# link

> 友情链接

{% method %}
**参数**

|参数名|必选|类型|默认值|含义|说明|
|:---:|:--:|:--:|:--:|:--:|:--:|
|type|否|number|`1`|类型|`1`-首页 `2`-内页 `3`-其他|
|orderby|否|string|`id desc`|排序|`asc`-正序 `desc`-倒序|
|limit|否|number|`10`|显示数量||
|flag|否|bool|`false`|标示|`true`-有图片 `false`-无图片|

{% sample lang="php" %}
**例子**

```html
<yhcms:flink type="1" limit="35" orederby="sort desc" flag="1" >
<li>
<a href="{$flink.url}">{$flink.name}</a>
</li>
</yhcms:flink>
```

>例子参数含义

>`type="1"`类型为"首页"

>`orderby="sort desc"`按照sort(排序字段)的倒序

>`limit="10"`显示10条信息

>`flag="1"`包含带图片的友情链接

{% endmethod %}