# SQL全称为：Structured Query language
# 有两种类型：
## 关联式资料库（SQL）---关联式数据库管理系统（RDBMS）
- MySQL
- Oracle
- PostgreSQL
- SQL Server

## 非关联式数据库（noSQL/no just SQL） ---非关联式数据库管理系统（NRDBMS）
- MoGoDB
- Redis
- DynamoDB
- Elaticsearch

## 部分英文翻译：
- primary key，主键，表唯一，避免重复
- foreign key 外键，让主键相对应，表与表相关键，用REFERENCES(参考)来表示链接哪个表对应属性
- 主要的属性资料形态
	- INT
	- DECIMAL(m,n)   表示有小数点的数，m为共有几位数，n为小数点后几位数
	- VARCHAR(n)，字符串，n为字数
	- BLOB  ,Binary Large Object，存放二进制的资料，图片视频等
	- DATA   以'YYYY-MM-DD'为格式的日期
	- TIMESTAMP  'YYYY-MM-DD  HH:MM:SS'，记录时间，数据写入，删除，修改的时间
- DROP  删除
- DESCRIBE  描述，显示（表）
- ALTER 修改表属性
- COLUMN  行
- INSERT INTO  添加
- UNIQUE 值唯一，不重复
- AUTO_INCREMENT  主键递增，但修改数据时，格式为前面带有属性
- ORDER BY  排序，默认为（ASC）低到高，DESC为高到低
- LIMIT  X，只取前x位
- 《》 为不等号
- DISTINCT  消除重复属性

