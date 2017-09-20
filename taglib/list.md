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
<yhcms:list cid="1" titlelen="20" orderby="sort desc" keyword="product" limit="10" pagesize="10" flag="c">
<li data-id="{$list.id}">
    <a href="{$list.url}"><img src="{$list.litpic}" alt="{$list.title}"></a>
    <a href="{$list.url}">{$list.title}{$list.publishtime|date='Y-m-d',###}</a>
    <p>{$list.description|str2sub=20, true}</p>
</li>
</yhcms:list>
```

>例子参数含义

><font color=#81a2be>`cid="1"`</font>栏目ID为1
* *指定内容信息所属的栏目具体ID值 或者 传入`$cid`将获取当前页面所属栏目ID*
   
>`titlelen="20"`标题截取20个字符

>`orderby="sort desc"`按照sort(排序字段)的倒序
* *其他可排序字段例如`id`,`publishtime`等*

>`keyword="product"`调取product(产品)
* *该功能主要用于搜索列表分类展示*

>`limit="10"`显示10条信息
* *当`pagesize`参数存在时该参数无效*

>`pagesize="10"`每10条分成一页
* *与`{$page}`配合使用*

>`flag="c"`只显示后台推荐的信息



{% endmethod %}