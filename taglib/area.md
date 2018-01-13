# area

> 地区导航

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|pid|上级id|number|`0`|设置未指定pid时默认使用pid `0`-读取所有顶级地区|
|top|是否推荐|bool|`false`|`false`-全部 `true`-开启推荐|
|con|独立内容|bool|`false`|`false`-全部 `true`-开启独立内容|
|url|二级域名|bool|`false`|`false`-全部 `true`-开启二级域名|
|limit|显示数量|number|`10`|&nbsp;|
|type|只读取当前地区信息|string|`group`|`group`-梯度显示 `current`-当前地区  `level`-平级|
|conurl|生成|number|`0`|`0`-根据当前页面自动生成URL `1`-根据首页URL情况生成|

**字段**

|字段名|别名|
|:----:|:--:|
|{$area.title}|名称|
|{$area.stitle}|缩写|
|{$area.etitle}|英文|
|{$area.sort}|排序|
|{$area.pid}|上级|
|{$area.istop}|推荐|
|{$area.iscon}|独立内容|
|{$area.isurl}|二级域名|

{% sample lang="php" %}
**例子**

```html
<yunu:area top="1" con="1" url="1" limit="20" type="group">
    <a href="{$area.url}">{$area.title}</a>
</yunu:area>
```

例子参数含义

>`top="1"`筛选出后台设置为推荐的

>`con="1"`筛选出后台设置为独立内容的

>`url="1"`筛选出后台设置为二级域名的

>`limit="20"`显示20条信息

>`type="group"`显示当前地区及子地区

{% endmethod %}
