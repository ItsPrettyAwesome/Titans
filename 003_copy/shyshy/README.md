
### 1. 如果 'open' 或者另外几个相关的系统调用执行出错，你如何找出出错的原因？

答：我们在编写代码，如 'open、read' 等调用时，会有 'errno' 字符，根据 'errno' 字符提示找出调用问题。

### 2. 你觉得学习本篇有什么困难？

答： 一开始纠结于 'open' 和 'read' 的返回值，上节没有学习好；
     这周忙着毕业论文，对这些文件指针、描述符不是很明白。就拖延到现在，书店淘了一本书;
     之后才搞懂这些关系。仔细翻了博主的系统编程博客。

### 3. 你觉得掌握文件 IO 还能做什么事情？

答： Linux，everything is file，我想能做很多，创建、修改、改变属性、文件通信；

### 4. 在你的终端执行命令 'ps' ，你会看到你当前 bash 的 PID 号(第一行)，记下这个 PID ,然后再执行 'lsof -p ${PID}' , 注意了，请把 '${PID}' 替换成你看到的 PID 。接下来你会看到 'lsof' 执行的输出结构。描述你看到的现象，你发现了什么？

答： 第一行表示我当前进程，'fd:cwd' ,表示 'current work directory' ；'rtd' 代表根目录，'txt' 代表执行程序;
     mem 代表映射内存文件；'TYPE' 列有三种：'DIR'（目录）、'REG'（普通文件）、'CHR' 、代表字符设备；
     最后bash进程打开了4个文件，分别 '0u,1u,2u.255u' ；0,1,2应该表示文件描述符，255查了也属于文件描述符，'u'意思可读可写。
