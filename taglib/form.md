#form

> 表单

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|fid|表单ID|number|`空`|对应后台的表单ID|
|orderby|排序|string|`无`||
|top |推荐|number|`无`||
|pagesize|分页|number|`无`||
|limit|显示数量|number|`无`||

{% sample lang="php" %}
**例子**

```html
<yunu:form fid="1">
</yunu:form>
```

>`fid="1"`获取后台表单ID为1的信息

{% endmethod %}