# catlist

> 栏目列表

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|cid|栏目ID|number|`必填`|后台栏目ID 或者 `$cid`-当前栏目id|
|type|类型|string|`son`|`son`-下级栏目 `self`-同级栏目 `top`-顶级栏目(此类型下cid可忽略) `parent`-当前栏目的顶级栏目|
|limit|显示数量|number|`10`||
|flag|标示|number|`1`|`0`-不显示外部链接和单页 `1`-全部|

**字段**

|别名|调用代码|
|:--:|:--:|
|栏目名称|{$catlist.title}|
|栏目副标题|{$catlist.subtitle}|
|栏目封面图|{$catlist.pic}|
|栏目链接|{$catlist.url}|
|栏目子栏目|{$catlist.child}|

{% sample lang="php" %}
**例子**

```html
<yunu:catlist cid="$category['id']" type="parent" limit="20" flag="0">
<li>
    <a href="{$catlist.url}">{$catlist.title}</a>
    <volist name="catlist['child']" id="v">
    <ul>
        <li><a href="{$v.url}">{$v.title}</a></li>
    </ul>
    </volist>
</li>
</yunu:catlist>
```

例子参数含义

>`cid="1"`当前栏目ID

>`type="parent"`类型为当前cid栏目的顶级栏目

>`limit="20"`显示20条信息

>`flag="0"`排除外部链接和单页

{% endmethod %}
