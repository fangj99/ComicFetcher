# ComicFetcher
A crawler to collect comics from http://comic.ck101.com

__Please go to [DriveIt](https://github.com/XIAZY/DriveIt), a smarter crawler I wrote which can support multiple websites.__
# Usage
Simply run this script with ```Python 3```. Input the regular expression and cover link when asked. The script will handle all the jobs.

All files are dowloaded in the same working directory with subdirectories named following _episodes_.

I completely understand that English-speaking people won't use this crawler. Just scroll down for Chinese explanation.
# 总览
这是一个用于下载 http://comic.ck101.com 上漫画的爬虫。估计也没什么人看我就随便写写了。

__请前往 [DriveIt](https://github.com/XIAZY/DriveIt)，我正在开发的一个更加智能好用、易于维护且支持多个网站的爬虫。__

需要 ``Python 3`` 和一些关于正则表达式的知识。
# 用法
首先找到你要下载的漫画的目录，比如说这样的：
![Cover Page](http://i.imgur.com/d0M6DSS.png)
~~这是个很正直的漫画。~~ 记下这个链接，我们将其称为 Cover Link.
查看源代码，找到链接到内页的部分。观察之，差不多长这样：
![Source](http://i.imgur.com/cRWtNdC.png)
我们按照这个格式写出正则表达式就好了，比如这样的：```\'\高\寮\物[\语|\語]\s(\d{3})\集\'\,\'\/vols/(\d{7})```
注意第```?```集和卷号 /vols/```???????``` 要用括号框起来，要不然爬虫会报错。

最后用 ```Python 3``` 运行爬虫，比如这样：
![Running](http://i.imgur.com/DK9BmB9.png)

等着吧。

如果在大陆需要全局梯子来运行这个爬虫，PAC 是不行的。当然如果有 ```proxychains``` 之类的玩意也很好。最好的应该还是直接在 OpenWrt 路由上配置。

本人学艺不精，如果有更好的实现还请发 Pull Request.
