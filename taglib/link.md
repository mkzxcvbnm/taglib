# link

> 友情链接

{% method %}
**参数**

|参数名|必选|类型|说明|
|:----:|:--:|:--:|:--:|
|type|是|number|类型|
|orderby|否|string|排序|
|limit|否|number|显示数量|
|flag|否|number|标示|

{% sample lang="php" %}
**例子**

```html
<yhcms:flink type="1" limit="35" orederby="sort desc" flag="1" >
  <li>
  <a href="{$flink.url}">{$flink.name}</a>
  </li>
</yhcms:flink>
```

>例子参数含义

>`type="1"`栏目ID为1
* *友情链接类型*

>`orderby="sort desc"`按照sort(排序字段)的倒序
* *其他可排序字段例如`id`,`publishtime`等*

>`limit="10"`显示10条信息
* *当`pagesize`参数存在时该参数无效*

>`flag="1"`只显示后台推荐的信息

{% endmethod %}