# config

> 读取配置信息

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|name|名称|string|`必填`|[点击查看](#name)|

<span id="name">**name**</span>

|别名|调用代码|
|:--:|:--:|
|SEO标题|`<yunu:config name="seo_title">`|
|SEO关键词|`<yunu:config name="seo_keywords">`|
|SEO描述|`<yunu:config name="seo_description">`|
|网站名称|`<yunu:config name="site_title">`|
|网站域名|`<yunu:config name="site_url">`|
|网站LOGO|`<yunu:config name="site_logo">`|
|网站ICO|`<yunu:config name="site_ico">`|
|版权信息|`<yunu:config name="site_copyright">`|
|手机LOGO|`<yunu:config name="wap_logo">`|
|手机版权信息|`<yunu:config name="wap_copyright">`|
|WAP站获取PC链接|`<yunu:config name="pcurl">`|
|PC站获取WAP链接|`<yunu:config name="wapurl">`|
|获取当前区域名称|`<yunu:area top="1" limit="1" type="current"> {$area.title} </yunu:area>`|

{% sample lang="php" %}
**例子**

```html
<yunu:config name="seo_title">
```

{% endmethod %}
