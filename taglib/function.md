# date

> 时间戳格式化

{% method %}

{% sample lang="php" %}
**例子**

```html
<yhcms:list cid="$cid">
    {$list.update_time|date='Y-m-d',###}
</yhcms:list>
```

**介绍**

```
{$list.update_time|date='Y-m-d',###}
```

>将`update_time`时间戳格式化成`年-月-日`格式
>`Y`-年 `m`-月 `d`-日 `H`-时 `i`-分 `s`-秒

{% endmethod %}

***

# str2sub

> 文字超出一定长度显示省略号

{% method %}

{% sample lang="php" %}

**例子**

```html
<yhcms:list cid="$cid">
    {$list.desc|str2sub=20, true}
</yhcms:list>
```

**介绍**

```
{$list.desc|str2sub=20, true}
```

>将`desc`截取20个字符，多余部分显示为省略号

{% endmethod %}

***

# str2arr

> 分割字符串为数组

{% method %}

{% sample lang="php" %}
**例子**

```html
<volist name="$content.mulimg|str2arr='***'" id="v">
    {$v}
</volist>
```

**介绍**

```
$content.mulimg|str2arr='***'
```

>使用`***`作为分隔符分割`$content.mulimg`字符串成数组 **!注意分隔符不能为竖线（|）**


{% endmethod %}
