# link

> 友情链接

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|type|类型|number|`1`|`1`-首页 `2`-内页 `3`-其他|
|orderby|排序|string|`id desc`|`asc`-正序 `desc`-倒序|
|limit|显示数量|number|`10`||
|flag|标示|bool|`不限制`|`true`-有图片 `false`-无图片|

**字段**

|别名|调用代码|
|:--:|:--:|
|名称|{$link.title}|
|图片|{$link.pic}|
|链接|{$link.url}|

{% sample lang="php" %}
**例子**

```html
<yunu:link type="1" limit="35" orederby="sort desc" flag="1" >
<a href="{$link.url}"><img src="{$link.pic}" alt="{$link.title}"></a>
</yunu:link>
```

例子参数含义

>`type="1"`类型为"首页"

>`limit="35"`显示35条信息

>`orderby="sort desc"`按照sort(排序字段)的倒序

>`flag="1"`包含带图片的友情链接

{% endmethod %}
