[TOC]

# Java Map简介

[Java Map 菜鸟教程](https://www.runoob.com/java/java-map-interface.html)

Map 集合类用于存储元素对（称作“键”和“值”），其中每个键映射到一个值。

在 java.util 常用的为： HashMap、Hashtable

# Java Map操作

```java
public class HelloMap {
    public static void demoMap() {
        // 初始化：HashMap<K,V> implements Map<K,V>
        Map<String, String> map = new HashMap<>();
      
        //获取大小
        System.out.println(map.size());

        //插入元素
        map.put("key1", "value1");
        map.put("key2", "value2");

        // //移除元素
        map.remove("key1");

        //清空map
        map.clear();

        System.out.println(map);
        System.out.println(map.size());
        System.out.println(map.get("key1"));
    }

    public static void main(String[] args) {
        // demoTable();
        demoMap();
    }
}

```