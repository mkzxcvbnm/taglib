# 内容页相关

* 上一篇/下一篇  其中的url和名称  prevurl/prevtitle
* {$content.url} 获取当前内容URL
* {$content.字段名}调用内容相关字段，通用字段和list调用同步

* {$content.url}调用当前内容URL

* {$content.prev}上一篇完整调用：示例 `<a href=”xxxx”>xxxx</a>`
* {$content.next}下一篇完整调用：示例 同上

* {$content.prevurl}上一篇单独URL
* {$content.prevtitle}上一篇单独标题
* {$content.nexturl}上一篇单独URL
* {$content.nexttitle}下一篇单独标题

* {$content.ys_title}调用未经地区信息处理过的原始标题

* {$category.字段名}调用当前分类信息，此调用仅限在列表页以及内容详情页调用
* {$parent.字段名}调用当前分类上级分类的信息，如果已经为顶级分类，则为null