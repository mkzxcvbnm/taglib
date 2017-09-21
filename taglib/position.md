# position

> 当前位置(面包屑导航)

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|cid|栏目ID|number|`必填`|后台栏目ID 或者 `$cid`-当前栏目id|
|sname|末尾链接名称|string|`空`||
|surl|末尾链接地址|string|`空`||
|delimiter|分隔符|string|`&gt;&gt;`|设置所有链接之间的间隔符|

{% sample lang="php" %}
**例子**

```html
<span>您的当前位置：</span>
<yunu:position cid="$cid" sname="当前页面" surl="javascript:;" delimiter="-" />
```

例子参数含义

>`cid="$cid"`获取当前页面的位置

>`sname="当前页面"`追加一个末尾链接,链接名称为"当前页面"

>`surl="javascript:;"`末尾链接地址为"javascript:;"

>`delimiter="-"`修改分隔符为"-"

{% endmethod %}
