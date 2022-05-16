# 具体题目

1. MySQL中有哪几种锁？

<details>

- 表锁：开销小，不会出现死锁。但是粒度大，并发度比较低。MyISAM使用表锁
- 页锁：介于表锁和行锁之间
- 行锁：粒度小，并发度高。但是开销大，容易出现死锁。InnoDB既支持表锁，也支持行锁，但是默认是行锁

</details>

2. 谈谈MySQL的几种存储引擎，区别是什么？

> https://blog.csdn.net/qq_35642036/article/details/82820178
<details>

- InnoDB支持事务；MyISAM不支持
- InnoDB支持外键；MyISAM不支持
- InnoDB是聚集索引；MyISAM是非聚集索引
- MyISAM有一个变量保存表的行数；InnoDB没有
- MyISAM支持全文检索；InnoDB在5.6版本后支持全文检索
- MyISAM只支持表级锁；InnoDB支持行级锁和表级锁，默认是行级锁
- InnoDB必须有唯一索引，MyISAM不需要
- InnoDB的文件有表定义文件、数据文件；MyISAM的文件有表定义文件、数据文件和索引文件

</details>

3. 什么是脏读、不可重复读、幻读？

> https://cloud.tencent.com/developer/article/1450773

4. 什么是聚集索引和非聚集索引

> https://www.cnblogs.com/aspnethot/articles/1504082.html


# 参考文献

1. https://github.com/caokegege/Interview/blob/master/db/%E6%9C%80%E5%85%A8MySQL%E9%9D%A2%E8%AF%9560%E9%A2%98%E5%92%8C%E7%AD%94%E6%A1%88.md