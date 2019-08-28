---
title: MySQL
date: 2016-06-14 17:56:42
tags:
---
1. Node.js怎么处理数据库中日期类型：
    我在MySql数据库中的日期是timestamp类型，可是查询出来显示在页面上之后就变成了: Fri May 17 2013 14:12:33 GMT+0800 (中国标准时间)
   这种格式，实际上数据库中显示的是： 2013-05-17 14:19:26
   能不能把页面上也显示这种格式啊，不要上面那种格式，敬请各位指教
   I am using mysql database,in that i have a field by name request_date. The type of the field is time stamp and the data stored in this field has the format 2012-05-16 14:59:18. But when I retrieve the same data by Node.JS, the data is displayed in the browser as

   Fri Jun 08 2012 15:16:50 GMT+0530 (India Standard Time)
   Why this format change is happening?

答：
   以我的php和node开发经验来看 关于日期时间 还是存储为时间戳的整数形式比较好 有的时候做一些 时间比较 或是时间查询（比如最近三个月的记录) 用时间戳显然要快一点 格式化还是交给客户端吧 感觉格式化后的数据对开发人员 没有什么实际意义 在mysql中DateTime 还要比Int多占一些空间（仅供参考）