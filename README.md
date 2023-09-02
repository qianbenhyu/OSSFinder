# OSSFinder
 Tools for discovering AKSK in mass assets
#EN#
Collaborate with crawler tools like RAD to discover OSS credentials in bulk
#CN#
配合rad这样的爬虫工具，批量发现oss凭据
通过RAD爬虫获取JS等目录的路径，保存到文件中。模糊查询，会有一些误报，但正则很好得匹配了各种可能的参数名（eg.ak/access_key-aliaccesskey）​。推荐在有大规模的资产中使用。小规模资产使用FindSomething或者burp中正则​匹配即可。
usage：
OSSFinder.exe -f URL.txt
