# url

> 获取url

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|name|名称|string|`必填`|[点击查看](#name)|

<span id="name">**name**</span>

|值|别名|说明|
|:-:|:--:|:--:|
|home|网站首页|生成网站首页网址|
|search|搜索页面|生成搜索页面网址|
|form|表单|表单提交URL|
|Captcha|验证码|验证码URL|

{% sample lang="php" %}
**例子**

```html
<yunu:url name="home">
<img src="<yunu:url name='captcha' id='1'>" onclick="this.src='<yunu:url name='captcha' id='1'>'" />  id为表单id
```

例子参数含义

>`name="home"`获取网站首页地址

{% endmethod %}
