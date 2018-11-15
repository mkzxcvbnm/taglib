#field

> 分类

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|id|自定义字段ID|number|`必填`|模型内自定义字段ID|
|group|分组|string|`必填`|ID分组 例如`131,132,133`|
|noset|不限|bool|`true`|`true`-显示"不限" `false`-不显示"不限"|
|active|活动|string|`active`|选中状态的class名|

**字段**

|字段名|别名|
|:----:|:--:|
|{$field.url}|链接|
|{$field.actice}|选中状态class名|
|{$field.name}|名称|

{% sample lang="php" %}

**例子**

```html
<yunu:field id="131" group="131,132,133" noset="true" active="active">
    <a href="{$field.url}" class="{$field.active}">{$field.name}</a>
</yunu:field>
```

**例子参数含义**

>`id="131"`自定义字段ID为131的信息

>`group="131,132,133"`ID分组为[131,132,133]

>`noset="true"`显示"不限"链接

>`active="active"`活动链接的class名为"active"

{% endmethod %}