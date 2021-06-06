
[TOC]

[JSON详细学习](https://www.w3cschool.cn/json/9l4f1h7u.html)

# Json简介

- JSON：JavaScript 对象表示法（JavaScript Object Notation）。

- JSON 是存储和交换文本信息的语法。类似 XML。

- JSON 比 XML 更小、更快，更易解析。是一种轻量级的数据交换格式。

- JSON 是纯文本

## Json数据结构

- JSON 支持以下两种数据结构：
  - **名/值对集合**： 关键字:值对（key:value）
  - **有序的值列表**： 包括数组，列表，向量或序列等等。

```josn
{
  "key": "value",
  "PI": 0.618,
  "arr": [1, 2, 3],
  "obj": {
    "x": 123,
    "y": 456
  }
}

<!-- 数组中多个对象 -->
{      
"employees": [        
{ "firstName":"John" , "lastName":"Doe" },        
{ "firstName":"Anna" , "lastName":"Smith" },        
{ "firstName":"Peter" , "lastName":"Jones" }        
]        
}
```

## Java获取Json方法



```java
package org.example.config;

import net.sf.json.JSONArray;
import net.sf.json.JSONObject;
import org.example.IO;

import java.util.HashMap;
import java.util.Map;


public class HelloJsonByJsonLib {
    public static void main(String[] args) {
        final String text = IO.readResourceText("/demo.json");
        assert null != text;

        // Map转JSON对象
        Map<String, Object> map = new HashMap<String, Object>();
        map.put("name", "张三");
        map.put("gender", false);
        JSONObject mapJson = JSONObject.fromObject(map);
        System.out.println(mapJson);

        // 字符串转JSON对象
        JSONObject textJson = JSONObject.fromObject(text);
        System.out.println(textJson);
        System.out.println(textJson.getString("key"));
        System.out.println(textJson.getDouble("PI"));
        JSONArray arr = textJson.getJSONArray("arr");
        System.out.println(arr.get(1));
        JSONObject obj = textJson.getJSONObject("obj");
        System.out.println(obj.getInt("x"));
        System.out.println(obj.getInt("y"));

        // 因为JSONObject实现了Map接口，所以可以像操作Map一样操作JSONObject
        // 编辑JSONObject
        obj.put("z", 789);
        System.out.println(obj);

        // JSON对象转化为字符串
        String resultText = textJson.toString();
        System.out.println(resultText);
    }
}
```

```Java
public static void main(String[] args) throws IOException {
        String text = readText();
        assert null != text;

        JSONObject json = JSONObject.fromObject(text);
        System.out.println(json.getString("key"));
        System.out.println(json.getDouble("PI"));
        JSONArray arr = json.getJSONArray("arr");
        System.out.println(arr.get(1));
        JSONObject obj = json.getJSONObject("obj");
        System.out.println(obj.getInt("x"));
        System.out.println(obj.getInt("y"));

        obj.put("z", 789);
        System.out.println(obj);

        String resultJson = json.toString();
        System.out.println(resultJson);
    }
```