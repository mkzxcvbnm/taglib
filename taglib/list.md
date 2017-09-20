#
list

> 内容列表

{% method %}
**参数**

|参数名|必选|类型|说明|
|:----:|:--:|:--:|:--:|
|cid|是|number|栏目ID|
|titlelen|否|number|标题长度|
|orderby|否|string|排序|
|keyword|否|string|关键词|
|limit|否|number|显示数量|
|pagesize|否|number|分页数|
|flag|否|number|标示|

{% sample lang="php" %}
**例子**

```html
<yhcms:list cid="1" titlelen="20" orderby="sort desc" keyword="product" limit="10" pagesize="10" flag="1">
<li data-id="{$list.id}">
    <a href="{$list.url}"><img src="{$list.litpic}" alt="{$list.title}"></a>
    <a href="{$list.url}">{$list.title}{$list.publishtime|date='Y-m-d',###}</a>
    <p>{$list.description|str2sub=20, true}</p>
</li>
</yhcms:list>
```

>例子参数含义

>`cid="1"`获取栏目ID为1的所有信息

>`titlelen="20"`标题截取20个字符

>`orderby="sort desc"`按照sort(排序字段)的倒序显示

>`keyword="product"`显示product(产品)的信息

>`limit="10"`显示10条信息

>`pagesize="10"`每页显示10条信息

>`flag="1"`包含带图片的友情链接

{% endmethod %}