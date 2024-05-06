这是我学习**tinyhttpd**的仓库，源代码来自[SourceForge](https://sourceforge.net/projects/tinyhttpd/)。

## 代码分析

我们一上来直接打开`httpd.c`，找到`main`函数。主函数一进去就是几个意义明确的局部变量，之后便是调用了`startup`函数。我们跳转到`startup`函数，先阅读该函数上方的注释，得知该函数是启动当前进程在指定端口监听web连接。

- todo: `startup`函数进一步分析

然后是一个死循环，进入之后，第一条语句是调用了`accept`函数，该函数的功能简单来说就是从服务器的socket中接受一个请求，并针对该请求创建一个新的socket。接下来便是创建一个线程执行`accept_request`函数。


