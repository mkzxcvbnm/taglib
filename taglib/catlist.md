# link

> 友情链接

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
|{$flink.id}|ID|
|{$flink.title}|标题|
|{$flink.pic}|图片|
|{$flink.url}|链接|
|{$flink.sort}|排序|
|{$flink.type}|类型|
|{$flink.area}|所属地区|

{% sample lang="php" %}
**例子**

```html
<yunu:catlist cid="1" type="self" limit="20" flag="0">
      <li>
          <a href="{$catlist.url}">{$catlist.title}</a>
          <volist name="catlist['child']" id="v">
              <ul>
                  <li><a href="{$v.id}">{$v.name}</a></li>
              </ul>
          </volist>
      </li>
</yunu:catlist>
```

例子参数含义

>`type="1"`类型为"首页"

>`limit="35"`显示35条信息

>`orderby="sort desc"`按照sort(排序字段)的倒序

>`flag="1"`包含带图片的友情链接

{% endmethod %}
