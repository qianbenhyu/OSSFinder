# OSSFinder_v2024.2.22

【2024.2.22版本】，工具旨在对指定目录下的敏感文件进行扫描，从中发现敏感信息。

## usage:

### OSSFinder.exe -m [a/b] -path [path]

```
-m a: 限制文件名和文件后缀，对含有"OSS", "aliyun", "config", "conf"等关键字 且 后缀为".txt", ".xml", ".php", ".json", ".cfg"等的文件进行扫描；

-m b：仅限制文件后缀，因此mode b能扫描更多文件。```

-path: 输入路径，注意在低权限用户运行时，可能没有某些路径的读取权限
```
## introduce:
正则匹配内容有
```OSS票据、bucket名、用户名/口令、微信CorpID、jdbc/redis/SSH/Telnet连接，xml格式的OSS票据、用户名/口令```

### 示例1：
原始文件
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/901f1c97-075a-418d-86cb-4a904ca939cb)

匹配效果
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/63418113-ebd8-4cda-ad4c-8466332db0cd)

### 示例2：
原始文件
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/d9277ec9-bb1c-467b-b9df-6c14800d7f60)
匹配效果
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/f8703a72-1bee-48df-865d-59f44d581381)

### 示例3：
原始文件
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/265ecd71-1af1-48e4-9e9d-8134280b7985)
匹配效果
![image](https://github.com/qianbenhyu/OSSFinder/assets/32768810/8d9156ce-49bd-4253-a7e5-f648a6a1f935)
