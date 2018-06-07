# tag

> tag

**使用方法**

> 如使用tag标签需要搭配创建模版页：tag_index.html
>
> 在模版页中使用list标签获取对应的数据，此处需设置：list 标签的tag参数值为"
$title"

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|title|tag值|string|``|可填写单个tag值或多个使用`,`逗号间隔 可为空，为空获取全站tag属性|
|limit|显示数量|number|`10`|&nbsp;|

**字段**

|字段名|别名|
|:----:|:--:|
|{$tag.url}|URL|
|{$tag.title}|单个tag值|
|{$tag.num}|tag出现次数|

{% sample lang="php" %}
**例子**

```html
<yunu:tag title="测试标签1,测试标签2,测试标签3">
     <a href="{$tag.url}"><span>{$tag.title}[{$tag.num}]</span></a>
</yunu:tag>
```

例子参数含义

>`title="测试标签1,测试标签2,测试标签3"` 获取tag值为`测试标签1`或`测试标签2`或`测试标签3`的内容

{% endmethod %}
