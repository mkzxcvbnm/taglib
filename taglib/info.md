#info

> 独立调用内容标签

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|conid|内容ID|number|`必填`|内容ID|
|type|类型|string|`必填`|`prev`(获取上一个)/`next`(获取下一个)|
|orderby|排序条件|string|`id`|排序条件|

{% sample lang="php" %}

**例子**

```html
<yunu:info conid="$content['id']" type="prev" orderby="id">
    上一篇：<a href="{$info.url}">{$info.title}</a>
</yunu:info>
<yunu:info conid="$content['id']" type="next" orderby="id">
    下一篇：<a href="{$info.url}">{$info.title}</a>
</yunu:info>
```

{% endmethod %}