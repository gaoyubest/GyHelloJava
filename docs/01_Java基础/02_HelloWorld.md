[TOC]

# HelloWorld

使用notepad编写HelloWorld程序后缀为.java

```java
// 单行注释
public class HelloWorld{
	public static void main(String[] args){
		System.out.println("Hello World!");
	}
}
/*  
多行注释
*/
```

## javac编译

- cmd进入HelloWorld.java所在目录

```bash
G:\HelloMD\GyHelloJava\arc>dir
 驱动器 G 中的卷是 课程+项目
 卷的序列号是 B87D-52B4

 G:\HelloMD\GyHelloJava\arc 的目录

2021/04/24  16:52    <DIR>          .
2021/04/24  16:52    <DIR>          ..
2021/04/24  16:52               112 HelloWorld.java
               1 个文件            112 字节
               2 个目录 42,403,332,096 可用字节
```

```bash

# 使用cmd javac编译完成，生成.class文件。注意此处有后缀。每次修改java代码后需要重新进行编译。
G:\HelloMD\GyHelloJava\arc>javac HelloWorld.java
```

![](./../images/05_HelloWorld.jpg)

## Java运行

```bash
# 使用cmd java运行程序。注意此处没有后缀。
G:\HelloMD\GyHelloJava\arc>java HelloWorld
Hello World!
```