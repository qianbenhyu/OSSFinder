配合rad这样的爬虫工具，批量发现oss凭据
通过RAD爬虫获取JS等目录的路径，保存到文件中。模糊查询，会有一些误报，但正则很好得匹配了各种可能的参数名（ak/access_key/aliaccess-key）​。推荐在有大规模的资产中使用。小规模资产使用FindSomething或者burp中正则​匹配即可。


usage：
OSSFinder.exe -f URL.txt

原始文件
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/b88c82bb-79cb-440f-9149-df1dd58fa3fe)
匹配效果
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/63418113-ebd8-4cda-ad4c-8466332db0cd)
