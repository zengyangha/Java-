# 点此回到[[JAVA（由此开始）]]

## 分类
- [[数组]]

## java集合框架提供一套好的、方便的接口和类，位于java.until包中

## 这是面向接口编程，其特性是能自动扩展

## 在集合中，如果要比较集合（或者判断集合中值是否相等），如果是自定义对象，会先查找对象中的equals和hashCode的方法，如果没有，则会比较地址（相当于=），要重写equals和hashCode方法才是比较内容[[Collection]]
- 因为hash类存储结构校验方式是先取hashcode判断是否相等，再取equals方法比较
- 重写equals就得要重写hashcode
- equals相等的，hashcode也相等
- hashcode不相等，equals也相等的
- 而hashcode相等，equals可能相等，也可能不相等的

## 有两大接口
- [[Collection]]
- [[Map]]

## List和Set是存储单列数据的集合，Map是存储键值的双列数据的集合

## 此外有个工具类名为：Collections，提供对集合进行排序，遍历等多种算法实现

