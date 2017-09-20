# list

> 内容列表

{% method %}
**参数**

|参数名|必选|类型|默认值|含义|说明|
|:---:|:--:|:--:|:--:|:--:|:--:|
|cid|是|number|`1`|栏目ID|后台栏目设置对应的ID `$cid`-当前栏目id|
|titlelen|否|number|标题长度||
|orderby|否|string|`id desc`|排序|`asc`-正序 `desc`-倒序|
|keyword|否|string|关键词|模糊查询title(标题)字段|
|limit|否|number|`10`|显示数量|当设置了`pagesize`时,该参数无效|
|pagesize|否|number|`10`|分页数|配合`{$page}`使用,生成分页|
|flag|否|bool|`false`|标示|`true`-推荐 `false`-全部|

{% sample lang="php" %}
**例子**

```html
<yhcms:list cid="1" titlelen="20" orderby="sort desc" keyword="yunu" limit="10" pagesize="10" flag="1">
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

>`keyword="yunu"`显示标题中包含`yunu`的所有信息

>`limit="10"`显示10条信息

>`pagesize="10"`每页显示10条信息

>`flag="1"`显示设置为`推荐`的信息

{% endmethod %}