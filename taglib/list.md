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

>下列代码将获取到 栏目ID为1 标题截取20个字符 按照sort(排序字段)的倒序 调取product(产品) 显示10条信息 每10条分成一页 只显示后台推荐的信息

```html
<yhcms:list cid="1" titlelen="20" orderby="sort desc" keyword="product" limit="10" pagesize="10" flag="c">
<li data-id="{$list.id}">
    <a href="{$list.url}"><img src="{$list.litpic}" alt="{$list.title}"></a>
    <a href="{$list.url}">{$list.title}{$list.publishtime|date='Y-m-d',###}</a>
    <p>{$list.description|str2sub=20, true}</p>
</li>
</yhcms:list>
```
{% endmethod %}