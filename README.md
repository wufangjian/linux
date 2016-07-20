##### linux
```
ps -aux | grep vui

netstat –apn | grep 8080


启动：netstat -tunlp |grep 8209


[文件的所属主以及所属组]
一个linux目录或者文件,都会有一个所属主和所属组。所属主,即文件的拥有者,而所属组,即该文件所属主所在的一个组.

================================================
[work@cp01-nativeads-fe.epc.baidu.com js]$ ls -l
总用量 8
-rw-r--r--  1 work work 7140  7月 20 15:12 ck.js


[work@cp01-nativeads-fe.epc.baidu.com tieba]$ ls -l
总用量 12
-rwxrwx---  1 work work  365  7月 20 11:40 config.php
drwxrwx---  2 work work 4096  7月 20 15:47 js
drwxrwx---  2 work work 4096  7月 19 21:09 layouts

第一列：权限
1 		描述文件类型[d:目录  -:普通文件 l:链接文件 b:表示该文件为块设备文件,比如磁盘分区 c:表示该文件为串行端口设备,例如键盘、鼠标]
2,3,4 	主
5,6,7   组
8,9,10	others

第二列：连接占用的节点(inode)
第三列：该文件的所属主
第四列：该文件的所属组
第五列：该文件大小
第六、七、八列：该文件创建日期或最近修改日期
第九列：文件名
================================================




1]更改文件所属主[用户] chown

chown work tieba


2]更改文件所属组[用户组] chgrp

chgrp work tieba


3]改变用户对文件的[读 r:4、写 w:2、执行 x:1 -:0]权限 chmod
	说明：在linux系统中,默认一个目录的权限为 755 = 7[user] + 5[group] + 5 [others],而一个文件的默认权限为644

chmod -r 777 tieba
```
