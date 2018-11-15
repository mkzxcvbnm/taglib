# config

> 读取配置信息

{% method %}
**参数**

|参数名|别名|类型|默认值|说明|
|:----:|:--:|:--:|:----:|:--:|
|name|名称|string|`必填`|[点击查看](#name)|

<span id="name">**name**</span>

|值|别名|对应后台设置|
|:----:|:--:|:--:|
|seo_title|SEO标题|**后台 > 扩展设置 > SEO设置**|
|seo_keywords|SEO关键词|同上|
|seo_description|SEO描述|同上|
|seo_hxkeyword|核心关键词|同上|
|seo_cwkeyword|长尾关键词|同上|
|site_title|网站标题|**后台 > 常用菜单 > 基础设置**|
|site_url|网站域名|同上|
|site_levelurl|二级域名后缀|同上|
|site_logo|网站LOGO|同上|
|site_copyright|版权信息|同上|
|site_guide|是否开启引导页|同上|
|theme_style|模板编号|同上|
|url_model|URL模式|**后台 > 常用菜单 > URL设置**|
|wap_auto|手机自动跳转|**后台 > WAP设置 > 基本设置**|
|wap_logo|手机网站LOGO|同上|
|wap_copyright|手机版权信息|同上|
|wap_levelurl|手机二级域名|同上|
|site_ico|网站ICO上传|-|
|pcurl|手机页面获取当前页面对应PC链接|-|

{% sample lang="php" %}
**例子**

```html
<yunu:config name="seo_title">
```
{% endmethod %}
