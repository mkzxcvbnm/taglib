# type

> 单个分类信息

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|typeid|栏目ID|number|`必填`|后台栏目ID 或者 `$cid`-当前栏目id|
|type|类型|string|`空`|`parent`-指定为typeid的顶级栏目|


**字段**

|字段名|别名|
|:----:|:--:|
|{$type.id}|ID|
|{$type.title}|分类名称|
|{$type.etitle}|别名|
|{$type.subtitle}|副标题|
|{$type.pid}|上级分类|
|{$type.mid}|所属模型|
|{$type.pic}|封面照片|
|{$type.seo_title}|SEO标题|
|{$type.seo_keyword}|SEO关键词|
|{$type.seo_desc}|SEO描述|
|{$type.jumpurl}|外部链接|
|{$type.tpl_cover}|封面模版|
|{$type.tpl_list}|列表模板|
|{$type.tpl_show}|内容模版|
|{$type.sort}|排序|
|{$type.status}|状态|
|{$type.target}|是否新窗口|
|{$type.type}|导航模式|
|{$type.desc}|栏目简介|
|{$type.content}|栏目内容|
|{$type.cover}|栏目属性|

{% sample lang="php" %}
**例子**

```html
<yunu:type typeid='21' type="parent">
    <a href="{$type.url}">查看更多</a>
</yunu:type>
```

例子参数含义

>`typeid="21"`获取栏目id为21的栏目信息

>`type="parent"`类型为当前typeid栏目的顶级栏目

{% endmethod %}
