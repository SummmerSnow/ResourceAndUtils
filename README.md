
# There is some resource link
***—————————————————————————————————————————————————***


## Recursive Neural network realized

[Tensorflow实现的Recursive neural network的实现例子1](https://github.com/vijayvee/Recursive-neural-networks-TensorFlow)

[Tensorflow实现的Recursive neural network的实现例子1](http://www.kdnuggets.com/2016/06/recursive-neural-networks-tensorflow.html)

[pytorch实现的Recursive:](http://ju.outofmemory.cn/entry/312166) 
## 本地关联远程git
- step1 注册创建自己的远程git账号
- step2 [在本地安装ssh和git](https://www.cnblogs.com/superGG1990/p/6844952.html)
- git pull origin master

添加文件，上传：
git add fileName
git commit -m "description"
git push origin master


## Linux 文件命令大全
统计命令
 wc -l #统计输出信息的行数，因为已经过滤得只剩一般文件了，所以统计结果就是一般文件信息的行数，又由于一行信息对应一个文件，所以也就是文件的个数
 grep "^-" #将长列表输出信息过滤一部分，只保留一般文件；如果只保留目录就是 ^d
 ls -lR #长列表输出该目录下文件信息(R代表recursive，对子文件夹进行搜索，可能是目录、链接、设备文件等)
 
 **统计某文件夹下目录的个数**
 ```
 ls -l |grep "^ｄ"|wc -l
 ```
 
 **统计某文件夹下目录的个数,包括子文件夹里的**
 ```
 ls -lR |grep "^ｄ"|wc -l
 ```
 
 **统计某文件夹下文件的个数**
 ```
 ls -l |grep "^-"|wc -l
 ```
 
**统计文件夹下文件的个数，包括子文件夹里的**
 ```
 ls -lR |grep "^ｄ"|wc -l
 ```
 
 **如统计/home/archer目录(包含子目录)下的所有js文件则：**
 ```
 ls -lR /home/archer|grep js|wc -l
 or:
  ls -lR "/home/archer"|grep "js"|wc -l
 ```
