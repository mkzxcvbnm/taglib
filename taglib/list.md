# list

> 内容列表

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|cid|栏目ID|number|`必填`|后台非单页模型栏目ID 或者 `$cid`-当前栏目id|
|titlelen|标题长度|number|`0`|`0`-不截取|
|orderby|排序|string|`id desc`|`asc`-正序 `desc`-倒序|
|keyword|关键词|string|`空`|模糊查询title(标题)字段|
|limit|显示数量|number|`10`|当设置了`pagesize`时,该参数无效|
|pagesize|分页数|number|`0`|配合`{$page}`使用,生成分页|
|flag|标示|bool|`false`|`true`-推荐 `false`-全部|
|top|头条|number|`0`|`0`-非头条 `1`-一级头条 ..... `9`-九级头条|
|tag|标签|string|`空`|增加LIST标签筛选条件，可直接输入中文，或使用"$content['tag']"使用当前详情页的|
|sql|分类范围|string|`空`|例如`"131 and 132 and 133"`and/or 必须配合 field 标签组合使用|
|area|指定地区|string|`空`|指定地区分类ID，获取该地区内容列表|
|image|获取带图内容|number|``| 默认获取所有，1获取带图内容|
|pagecss|分页样式|string|`1`| 1-带分页样式，0-不带分页样式|

**字段**

|别名|调用代码|
|:--:|:--:|
|标题|{$list.title}|
|副标题|{$list.ftitle}|
|缩略图|{$list.pic}|
|多图第一张|{$list.content\|str2img='1'}|
|简介截取|{$list.desc\|str2sub=60, true}|
|内容截取|{$list.content\|str2sub=60, true}|
|来源|{$list.source}|
|作者|{$list.author}|
|浏览量|{$list.click}|
|创建时间|{$list.create_time\|date='Y-m-d',###}|
|更新时间|{$list.update_time\|date='Y-m-d',###}|
|链接|{$list.url}|

**自定义模型字段**
>**自定义模型字段在 后台 > 系统管理 > 模型管理 > 字段管理 中查看**

{% sample lang="php" %}

**完整例子**

> 注意：例子包含所有参数只是为了说明展示 请根据实际需求选择需要的参数
>
>>不正确的参数可能导致程序报错
>
>>多余或组合错误的参数可能导致信息无法显示

```html
<yunu:list cid="1" titlelen="20" orderby="sort desc" keyword="yunu" limit="10" pagesize="10" flag="1" top="1" tag="1">
<li data-id="{$list.id}">
<a href="{$list.url}"><img src="{$list.pic}" alt="{$list.title}"></a>
<a href="{$list.url}">{$list.title}{$list.update_time|date='Y-m-d',###}</a>
<p>{$list.desc|str2sub=20, true}</p>
</li>
</yunu:list>
```

**例子参数含义**

>`cid="1"`获取栏目ID为1的信息

>`titlelen="20"`标题截取20个字符

>`orderby="sort desc"`按照sort(排序字段)的倒序显示

>`keyword="yunu"`显示标题中包含`yunu`的所有信息

>`limit="10"`显示10条信息

>`pagesize="10"`每页显示10条信息

>`flag="1"`显示设置为`推荐`的信息

>`top="1"`筛选出一级头条信息

>`tag="1"`此属性只在详情页生效 筛选出与当前信息tag的所有信息

**例子涉及函数**

* [date方法](/taglib/function.md#date)
* [str2sub方法](/taglib/function.md#str2sub)

{% endmethod %}
