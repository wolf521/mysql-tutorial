# 史上最简单的 MySQL 教程（十七）「索引」

## 索引

索引：**系统根据某种算法，将已有的数据（未来可能新增的数据），单独建立一个文件，这个文件能够实现快速匹配数据，并且能够快速的找到对应的记录**，几乎所有的索引都是建立在字段之上的。

索引的意义：

 - 提升查询数据的效率；
 - 约束数据的有效性。

但是增加索引是有前提条件的，这是因为索引本身会产生索引文件（有的时候可能会比数据本身都大），因此非常耗费磁盘空间。

 - 如果某个字段需要作为查询的条件经常使用，可以使用索引；
 - 如果某个字段需要进行数据的有效性约束，也可以使用索引（主键或唯一键）。

MySQL 中提供了多种索引，包括：

 1. 主键索引`primary key`
 2. 唯一键索引`unique key`
 3. 全文索引`fulltext index`
 4. 普通索引`index`

其中，主键和唯一键咱们之前已经了解过啦！至于普通索引，顾名思义，并没有什么特色，唯一的任务就是加快数据的查询速度。

在这里，咱们说说全文索引。全文索引，即根据文章内部的关键字进行索引，其最大的难度就是在于如何确定关键字。对于英文来说，全文索引的建立相对容易，因为英文的两个单词之间有空格；但是对于中文来说，全文索引的建立就比较难啦，因为中文两个字之间不仅没有空格，而是还可以随意组合。


----------
———— ☆☆☆ —— [返回 -> 史上最简单的 MySQL 教程 <- 目录](https://github.com/guobinhit/mysql-tutorial/blob/master/README.md) —— ☆☆☆ ————
