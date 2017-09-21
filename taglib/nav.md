# nav

> 导航

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|typeid|类型|number|`必填`|`1`-主导航 `2`-尾导航 `3`-全部|
|limit|显示数量|number|`10`||

**字段**

|字段名|别名|
|:----:|:--:|
|{$nav.id}|ID|
|{$nav.title}|分类名称|
|{$nav.etitle}|别名|
|{$nav.subtitle}|副标题|
|{$nav.pid}|上级分类|
|{$nav.mid}|所属模型|
|{$nav.pic}|封面照片|
|{$nav.seo_title}|SEO标题|
|{$nav.seo_keyword}|SEO关键词|
|{$nav.seo_desc}|SEO描述|
|{$nav.jumpurl}|外部链接|
|{$nav.tpl_cover}|封面模版|
|{$nav.tpl_list}|列表模板|
|{$nav.tpl_show}|内容模版|
|{$nav.sort}|排序|
|{$nav.status}|状态|
|{$nav.target}|是否新窗口|
|{$nav.nav}|导航模式|
|{$nav.desc}|栏目简介|
|{$nav.content}|栏目内容|
|{$nav.cover}|栏目属性|

**附加字段**

|字段名|别名|
|:----:|:--:|
|{$nav.child}|子栏目|

{% sample lang="php" %}
**例子**

```html
<yunu:nav typeid="1" limit="20">
<li>
    <a href="{$nav.url}">{$nav.title}</a>
    <volist name="nav['child']" id="v">
    <ul>
        <li><a href="{$v.url}">{$v.title}</a></li>
    </ul>
    </volist>
</li>
</yunu:nav>
```

例子参数含义

>`cid="1"`显示"导航栏显示"为"主导航"或"都显示"的栏目

>`limit="20"`显示20条信息

{% endmethod %}
