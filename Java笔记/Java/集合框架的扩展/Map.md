# 点此回到[[（十分重要）集合框架（java容器,集合类）]]

## 特点：key-value映射，相当于给每个值索引，根据key获取value

## Map自动扩容
- 1、设置值，计算Hash
- 2、扩容操作
- 3、数据迁移过程

## HashMap
- Key  无序，唯一
- Value  无序，不唯一
- Key和Value都可允许为空
- 底层结构为Hash表（一个动态数组）
- 在jdk1.7中，HashMap的数据结构为数据+链表，在jdk1.8后HashMap的数据结构为数据+链表+红黑树，（在1.8中，如果链表大于等于7，自动转换红黑树，节点叫Node类）
- 线程不安全，效率高

## Hashtable
- 线程安全，效率低
- Key和Value都  不 可允许为空

## LinkedHashMap
- 相当于有序的HashMap，多了个双向链表结构，这个链表可以按照元素的插入顺序或访问顺序进行排序，（有序）

## TreeMap
- 有序，但没HashMap快

## Map和Set的关系
- 采用相同的数据结构，哈希表
- Set是一种集合，存储不重复的元素，而Map是一种映射，存储键值对
- Set只存储元素值，而Map存储键值对，所以Set无序，Map有序
- Map的key是唯一，Set的元素是唯一

