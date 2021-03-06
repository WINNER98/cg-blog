# java.util.zip.ZipException: error in opening zip file

1 异常描述
------

在从 SVN 检出项目并配置完成后，启动 Tomcat 服务器，报出如下错误：

![zipe](http://img.blog.csdn.net/20170712144138152)

2 异常原因
------

通过观察上图中被标记出来的异常信息，咱们可以知道

> java.util.zip.ZipException: error in opening zip file

此异常，为：**打开`zip`文件异常**。

实际上，咱们观察错误信息的上面一行，即警告部分的时候，就可以发现引起这个异常发现的原因很可能就是位于 Tomcat 安装文件目录中`lib`文件夹下的`._tomcat-util.jar!`文件读取失败或者读取错误。



3 解决方法
------

在上述项目中使用的 Tomcat 为博主从 Mac 电脑中直接复制到 Windows 电脑中的，不知道是否是 Mac 电脑在项目运行的时候会自动生成一些只有其自己能够识别的文件，从而导致在移植过后，读取失败。但实际上，在博主删除相应的`.XXX`隐藏文件之后，这个异常确实解决啦！


----------

**温馨提示**：此异常的解决案例并没有很强的说服力，仅做参考，如果大家有更好的解决方法，欢迎分享给大家，非常感谢！


----------
———— ☆☆☆ —— [返回 -> 超实用的「Exception」和「Error」解决案例 <- 目录](https://github.com/guobinhit/cg-blog/blob/master/articles/solutioncase/README.md) —— ☆☆☆ ————