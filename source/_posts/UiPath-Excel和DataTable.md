---
title: UiPath Excel和DataTable
date: 2018-10-28 16:47:37
tags: RPA
---
1. 总是在**Excel Application Scope**中，这是一个容器（Container）；
1. **visible property**: 能否看到对excel的操作以及机器是否需要安装Excel；最好还是visible的，因为这样debug的时候也比较容易；
![对比](https://upload-images.jianshu.io/upload_images/2956070-fb61e7f73fb10e01.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
1. Excel/Worksheet可能是任何形式的数据，比如：文字，图片；
	Data table: 最简单的电子表格数据：行、列、标题；
1. **Read Range**: range 可以为空； 当AddHeaders 属性被选中的时候，是告知UiPath第一行是Headers;
![](https://upload-images.jianshu.io/upload_images/2956070-4fd56fb1f1e399ef.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
输出结果：
![](https://upload-images.jianshu.io/upload_images/2956070-3a82fceed4bdf205.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

1. **Write Range**: 在Write Range活动这里，当AddHeaders 属性被选中的时候，是告知UiPath把第一行写到excel中；![](https://upload-images.jianshu.io/upload_images/2956070-9f2f62644adcac1c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

1. **Sort Table**: read range 和write range的AddHeaders属性都要被选中，这样写到excel中的数据就是有header而且可以sort的，当然excel本身也要插入表。
![](https://upload-images.jianshu.io/upload_images/2956070-beb4813e8a9cb455.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![插入表](https://upload-images.jianshu.io/upload_images/2956070-8f0308679989ac2c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
1. **Build Data Table**: 为表添加每一列列名和数据类型，然后添加行数据；
1. **Output data table**:可以把data table转换成字符串，然后就可以输出。
1. **数组**
![数组.png](https://upload-images.jianshu.io/upload_images/2956070-8247ff1755cd815a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
