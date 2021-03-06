
## Linux 文件命令大全

### =============== 统计命令 ===============
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


### =============== 文件夹解压、复制 ===============
https://www.cnblogs.com/manong--/p/8012324.html

#### 文件复制
cp fileName target-directory
cp -r directory_name target-directory
-r 表示递归的操作，一般用于文件夹上的操作；
不清楚每个参数的含义的时候，可以使用  man command 查看命令的具体使用方法。



## cut 命令
cut 默认以制表符为分隔符
https://www.cnblogs.com/Spiro-K/p/6361646.html



### =============== 统计磁盘信息 ===============
显示当前文件件下文件大小：
du -sh *
du -s *

显示当前文件下文件大小，并根据文件大小进行排序：
du -s * | sort -nr
