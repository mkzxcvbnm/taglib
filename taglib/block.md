# block

> 自定义块

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|name|标题|string|`必填`|自定义块名称|
|infolen|内容长度|number|`0`|`0`-不截取 **注意：**图片或丰富类型自定义块勿使用此属性|
|textflag|内容类型|bool|`false`|`true`-输出为img `false`-输出内容|

{% sample lang="php" %}
**例子**

```html
<yunu:block name="文字自定义块1" infolen="100"></yunu:block>
<yunu:block name="丰富自定义块1"></yunu:block>
<yunu:block name="图片自定义块1" textflag="1"></yunu:block>
<img class="" src="<yunu:block name="图片自定义块2"></yunu:block>" alt="">
```

例子参数含义

>`name="自定义块1"`获取"自定义块1"的内容

>`infolen="100"`结果截取100个字符 \***infolen参数只应该在后台自定义块类型为文字时使用**\*

>`textflag="1"`输出为img标签,img的src属性为自定义块的内容

{% endmethod %}
