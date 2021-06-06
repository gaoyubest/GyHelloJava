# yaml

## 基本语法规则

- 大小写敏感
- 使用缩进表示层级关系
- 缩进时不允许使用Tab键，只允许使用空格。
- 缩进的空格数目不重要，只要相同层级的元素左侧对齐即可
- "#": 表示注释，从这个字符一直到行尾，都会被解析器忽略

## YAML 支持的数据结构有三种

- 对象：键值对的集合，又称为映射（mapping）/ 哈希（hashes） / 字典（dictionary）
- 数组：一组按次序排列的值，又称为序列（sequence） / 列表（list）
- 纯量（scalars）：单个的、不可再分的值

```py
    public static void main(String[] args) throws IOException {
        //读yaml文件
        String text = IO.readResourceText("/demo.yaml");
        Yaml yaml = new Yaml();
        //获取对象
        Map<Object, Object> obj = yaml.load(text);
        //获取列表
        List<Object> list = (List<Object>) obj.get("depart");
        //获取列表中第一个对象 {}内为对象，[]内为列表
        Map<Object, Object> one = (Map<Object, Object>) list.get(0);

        System.out.println(obj);
        System.out.println(list);
        System.out.println(one);
        System.out.println(one.get(0));
        System.out.println(one.get("id"));
        System.out.println(one.get("name"));
        System.out.println(one.get("salary"));
    }

```