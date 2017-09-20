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

**字段**

|字段名|别名|
|:----:|:--:|
|{$list.id}|ID|
|{$list.cid}|栏目ID|
|{$list.mid}|模型ID|
|{$list.title}|标题|
|{$list.jumpurl}|外链|
|{$list.etitle}|别名|
|{$list.click}|浏览量|
|{$list.vid}|更多字段ID|
|{$list.sort}|排序|
|{$list.istop}|推荐|
|{$list.create_time}|创建时间|
|{$list.update_time}|更新时间|
|{$list.aid}|管理员ID|
|{$list.seo_title}|SEO标题|
|{$list.seo_keywords}|SEO关键词|
|{$list.seo_desc}|SEO描述|
|{$list.area}|城市|

**附加字段**

|字段名|别名|
|:----:|:--:|
|{$list.alltitle}|标题全称|
|{$list.url}|链接地址|

**产品模型字段**

|字段名|别名|
|:----:|:--:|
|{$list.pic}|缩略图|
|{$list.price}|价格|
|{$list.desc}|简介|
|{$list.content}|内容|

**文字模型字段**

|字段名|别名|
|:----:|:--:|
|{$list.source}|来源|
|{$list.author}|作者|
|{$list.desc}|简介|
|{$list.content}|内容|

**自定义模型字段**
>**自定义模型字段在 后台 > 系统管理 > 模型管理 > 字段管理 中查看**

{% sample lang="php" %}
**例子**

```html
<yhcms:list cid="1" titlelen="20" orderby="sort desc" keyword="yunu" limit="10" pagesize="10" flag="1">
<li data-id="{$list.id}">
<a href="{$list.url}"><img src="{$list.litpic}" alt="{$list.title}"></a>
<a href="{$list.url}">{$list.title}{$list.update_time|date='Y-m-d',###}</a>
<p>{$list.desc|str2sub=20, true}</p>
</li>
</yhcms:list>
```

**例子参数含义**

>`cid="1"`获取栏目ID为1的信息

>`titlelen="20"`标题截取20个字符

>`orderby="sort desc"`按照sort(排序字段)的倒序显示

>`keyword="yunu"`显示标题中包含`yunu`的所有信息

>`limit="10"`显示10条信息

>`pagesize="10"`每页显示10条信息

>`flag="1"`显示设置为`推荐`的信息

**例子字段处理函数解释**

```
{$list.update_time|date='Y-m-d',###}
```

>将`update_time`字段时间戳格式化 `Y`-年 `m`-月 `d`-日 `H`-时 `i`-分 `s`-秒

```
{$list.desc|str2sub=20, true}
```

>截取简介20个字符超出部分显示为"..."

{% endmethod %}
