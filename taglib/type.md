# type

> 单个分类信息

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|typeid|栏目ID|number|`必填`|后台栏目ID 或者 `$cid`-当前栏目id|
|type|类型|string|`空`|`parent`-指定为typeid的顶级栏目|


**字段**

|别名|调用代码|
|:--:|:--:|
|栏目名称|{$type.title}|
|栏目副标题|{$type.subtitle}|
|栏目封面图|{$type.pic}|
|栏目链接|{$type.url}|
|栏目子栏目|{$type.child}|

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
