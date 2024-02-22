【2024.2.22版本】，工具旨在对指定目录下的敏感文件进行扫描，从中发现敏感信息。

usage:
OSSFinder.exe -m [a/b] -path [path]

-m a: 限制文件名和文件后缀，对含有"OSS", "aliyun", "config", "conf"等关键字 且 后缀为".txt", ".xml", ".php", ".json", ".cfg"等的文件进行扫描；

-m b：仅限制文件后缀，因此mode b能扫描更多文件。

-path: 输入路径，注意在低权限用户运行时，可能没有某些路径的读取权限

正则匹配内容有 OSS票据、bucket名、用户名/口令、微信CorpID、jdbc/redis/SSH/Telnet连接，xml格式的OSS票据、用户名/口令

示例1：
原始文件
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/b88c82bb-79cb-440f-9149-df1dd58fa3fe)
匹配效果
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/63418113-ebd8-4cda-ad4c-8466332db0cd)


【其他版本】
配合rad这样的爬虫工具，批量发现oss凭据
通过RAD爬虫获取JS等目录的路径，保存到文件中。模糊查询，会有一些误报，但正则很好得匹配了各种可能的参数名（ak/access_key/aliaccess-key）​。推荐在有大规模的资产中使用。小规模资产使用FindSomething或者burp中正则​匹配即可。


usage：
OSSFinder.exe -f URL.txt
