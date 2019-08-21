#内容页相关

> {$content.字段名}调用内容相关字段，通用字段和list调用同步

|别名|调用代码|
|:--:|:--:|
|标题|{$content.title}|
|副标题|{$content.ftitle}|
|缩略图|{$content.pic}|
|简介截取|{$content.desc\|str2sub=60, true}|
|内容截取|{$content.content\|str2sub=60, true}|
|来源|{$content.source}|
|作者|{$content.author}|
|浏览量|{$content.click}|
|创建时间|{$content.create_time\|date='Y-m-d',\#\#\#}|
|更新时间|{$content.update_time\|date='Y-m-d',\#\#\#}|
|链接|{$content.url}|
|上一篇|{$content.prev}|
|下一篇|{$content.next}|
|上一篇链接|{$content.prevurl}|
|上一篇标题|{$content.prevtitle}|
|下一篇链接|{$content.nexturl}|
|下一篇标题|{$content.nexttitle}|
|未经处理的原始标题|{$content.ys_title}|
|调用当前分类信息|{$category.字段名}|
|调用当前分类上级分类的信息|{$parent.字段名}|