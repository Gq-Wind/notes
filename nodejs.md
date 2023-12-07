# nodejs

## fs文件系统模块

> Node.js官方提供的 用来操作文件的模块 提供了一系列的方法和属性,用来满足用户对文件操作的需求

```
const fs =require('fs');

fs.readFile(path[,options],callback)	//文件路径 读取文件的编码格式  回调函数

fs.writeFile(path,data[,options],callback)	文件路径 内容 写入格式 回调
```

使用相对路径,执行node命令时所处目录动态拼接出被操作文件的完整路径;解决方案:直接使用完整路径,但这样移植性非常差,不利于维护. 

node中用`__dirname`表示文件所处的目录

