# catlist

> 栏目列表

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|cid|栏目ID|number|`必填`|后台栏目ID 或者 `$cid`-当前栏目id|
|type|类型|string|`son`|`son`-下级栏目 `self`-同级栏目 `top`-顶级栏目(此类型下cid可忽略)|
|limit|显示数量|number|`10`||
|flag|标示|number|`1`|`0`-不显示外部链接和单页 `1`-全部|

**字段**

|字段名|别名|
|:----:|:--:|
|{$catlist.title}|分类名称|
|{$catlist.etitle}|别名|
|{$catlist.subtitle}|副标题|
|{$catlist.pid}|上级分类|
|{$catlist.mid}|所属模型|
|{$catlist.pic}|封面照片|
|{$catlist.seo_title}|SEO标题|
|{$catlist.seo_keyword}|SEO关键词|
|{$catlist.seo_desc}|SEO描述|
|{$catlist.jumpurl}|外部链接|
|{$catlist.tpl_cover}|封面模版|
|{$catlist.tpl_list}|列表模板|
|{$catlist.tpl_show}|内容模版|
|{$catlist.sort}|排序|
|{$catlist.status}|状态|
|{$catlist.target}|是否新窗口|
|{$catlist.nav}|导航模式|
|{$catlist.desc}|栏目简介|
|{$catlist.content}|栏目内容|
|{$catlist.cover}|栏目属性|

**附加字段**

|字段名|别名|
|:----:|:--:|
|{$catlist.child}|子栏目|

{% sample lang="php" %}
**例子**

```html
<yunu:catlist cid="1" type="self" limit="20" flag="0">
<li>
    <a href="{$catlist.url}">{$catlist.title}</a>
    <volist name="catlist['child']" id="v">
    <ul>
        <li><a href="{$v.id}">{$v.title}</a></li>
    </ul>
    </volist>
</li>
</yunu:catlist>
```

例子参数含义

>`cid="1"`栏目id为1

>`type="self"`同级栏目

>`limit="20"`显示20条信息

>`flag="0"`排除外部链接和单页

{% endmethod %}
