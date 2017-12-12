# IntellJ-IDEA-ClassJavaLauchHelp
## idea 启动Class JavaLaunchHelper is implemented in both...Error解决
在IDEA启动的时候会报一个Class JavaLaunchHelper is implemented in both的错误
```java
objc[823]: Class JavaLaunchHelper is implemented in both /Library/Java/JavaVirtualMachines/jdk1.8.0_131.jdk/Contents/Home/bin/java (0x10ede24c0) and /Library/Java/JavaVirtualMachines/jdk1.8.0_131.jdk/Contents/Home/jre/lib/libinstrument.dylib (0x10ee664e0). One of the two will be used. Which one is undefined.
[ERROR] Error executing Maven.
```
大概意思是说这是Mac上面Java的一个老Bug了，会在那些使用了Java Agent的IDE上运行应用时触发，但这个Error对程序是无影响的，可以无视。在Java 9和Java 1.8.152版本里已经修复了。
#### 解决方案
#### 点击工具栏Help ----Edit Custom Properties，没有这个properties文件的话，IJ会提示创建，然后在里面加上
```java
idea.no.launcher=true
```
 然后重新启动IDEA即可
