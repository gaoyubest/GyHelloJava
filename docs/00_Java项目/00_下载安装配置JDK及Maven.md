[TOC]

## 1、安装和配置Java

### JDK下载

[点击下载JDK11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)

### JDK安装

- 取消外部公共JRE
![](./images/02安装jdk.jpg)

- 修改安装路径，路径中不能含有空格或者中文
- 安装完成后在bin目录中

### JDK环境配置

```bash
添加系统变量：
变量名：JAVA_HOME
变量值：D:\Java\jdk1.8.0_231
添加路径Path：
D:\Java\jdk1.8.0_231\bin
```

![](./images/03环境配置.jpg)

- 查看是否安装成功

```bash
C:\Users>java -version

java version "1.8.0_231"
Java(TM) SE Runtime Environment (build 1.8.0_231-b11)
Java HotSpot(TM) 64-Bit Server VM (build 25.231-b11, mixed mode)

C:\Users>javac -version
javac 1.8.0_231
```

## 2、安装和配置Maven

[点此配置Maven及阿里云镜像https://blog.csdn.net/a805814077/article/details/100545928](https://blog.csdn.net/a805814077/article/details/100545928)
