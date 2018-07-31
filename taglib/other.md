#内容页相关

> {$content.字段名}调用内容相关字段，通用字段和list调用同步

|字段名|别名|
|:----:|:--:|
|{$content.id}|ID|
|{$content.cid}|栏目ID|
|{$content.mid}|模型ID|
|{$content.title}|标题|
|{$content.jumpurl}|外链|
|{$content.etitle}|别名|
|{$content.click}|浏览量|
|{$content.vid}|更多字段ID|
|{$content.sort}|排序|
|{$content.istop}|推荐|
|{$content.create_time}|创建时间|
|{$content.update_time}|更新时间|
|{$content.aid}|管理员ID|
|{$content.seo_title}|SEO标题|
|{$content.seo_keywords}|SEO关键词|
|{$content.seo_desc}|SEO描述|
|{$content.area}|城市|
|{$content.url}|调用当前内容URL|
|{$content.prev}|上一篇完整调用：示例 `<a href=”xxxx”>xxxx</a>`|
|{$content.next}|下一篇完整调用：示例 同上|
|{$content.prevurl}|上一篇单独URL|
|{$content.prevtitle}|上一篇单独标题|
|{$content.nexturl}|下一篇单独URL|
|{$content.nexttitle}|下一篇单独标题|
|{$content.ys_title}|调用未经地区信息处理过的原始标题|
|{$category.字段名}|调用当前分类信息，此调用仅限在列表页以及内容详情页调用|
|{$parent.字段名}|调用当前分类上级分类的信息，如果已经为顶级分类，则为null|