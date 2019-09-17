# WallpapersWideSpider
download wallpaper
* #### 壁纸爬虫
* #### 学习总结

    * 分析wallpaperswide网站页面结构
    * 通过分析得出通过该网站首页存在不同壁纸的分类信息
    * 爬取该分类信息，进入不同的分类页面可以发现不同分类页面的地址存在规律
    * 进入具体分类页面，每个分类页面会集中展示该分类下的10张壁纸
    * 通过分析具体壁纸下载请求，可以根据该壁纸的名字构造出该壁纸的下载链接
    * 通过请求该下载链接，即可将响应内容保存至本地(响应内容为图片格式的文件)
* #### 不足
    * 该壁纸网站存在不同分类下的分辨率不同壁纸，只能手动设置抓取某分辨率下的壁纸
    * 采用多线程，没有考虑线程池，会持续生成线程任务
    * 没有对访问时间做限制，可能该网站没有对请求对象做反爬处理，会在短时间内生成大量请求，有可能会造成ip封禁
    * 仍然是一个简单的过程式编程，没有用到面向对象的思想，待之后改进
* #### 使用
    
    * 安装两个python库
        * requests
        * lxml(采用xpath来提取具体信息)
    * 运行main.py文件,保存的壁纸文件会在download文件夹下，不同分类的壁纸会生成特定文件夹