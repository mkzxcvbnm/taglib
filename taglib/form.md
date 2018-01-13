#form

> 

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|fid|上级id|number|`0`|设置未指定pid时默认使用pid `0`-读取所有顶级地区|
|orderby|排序|string|`id desc`|`asc`-正序 `desc`-倒序|
|top |||||
|pagesize|分页数|number|`0`|配合`{$page}`使用,生成分页|
|limit|显示数量|number|`10`|当设置了`pagesize`时,该参数无效|

{% sample lang="php" %}
**例子**

```html
<yunu:form fid="" orderby="" top="" pagesize="" limit="">
</yunu:form>
```

{% endmethod %}