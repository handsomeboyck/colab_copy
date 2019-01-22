```sql
-- 单表查询
SELECT * FROM `user`;
-- 排序查询
-- 降序
SELECT * FROM `user` ORDER BY number DESC;
-- 升序排列 默认
SELECT * FROM `user` ORDER BY number ASC;
-- number 优先级高于 dgh ,当前面的条件值一样是才会判断第二条件
SELECT * FROM `user` ORDER BY number ASC,dgh DESC;
 
--  聚合查询 ---将一列数据作为一个整体用来‘纵向’计算
-- count 计算数量个数 SELECT count(列名) from 表名 null值默认不计入
SELECT count(name) FROM `user`; 
-- null值也计入的解决方案 ，一般选择非空的值进行count（主键），或者 count(*),不推荐使用，查询效率差
SELECT count(IFNULL(weight,0)) FROM `user`;
-- sum  和
SELECT SUM(weight) FROM `user`;
-- max  计算最大值
SELECT max(weight) FROM `user`;
-- min   计算最小值
SELECT min(weight) from `user`;
-- avg   计算平均值
SELECT AVG(weight) FROM `user`;

-- 分组查询 SELECT 聚合函数（列名）/分组字段 GROUP BY 分组字段
SELECT `name` FROM `user` GROUP BY `name`; 
SELECT count(`name`) FROM `user` GROUP BY `name`;
-- 分组前对条件进行限定Where
SELECT `name` FROM `user` WHERE number>10 GROUP BY `name`;
-- 分组之后对条件进行限定Having
SELECT `name` FROM `user`  GROUP BY `name` HAVING COUNT(`name`)>2;
-- WHERE 和 HAVING的区别
-- 1.WHERE 在分组前进行条件判断，HAVING在分组完成后进行条件判断
-- 2.HAVING 后可使用聚合函数 ，WHERE 不行

-- 总结
-- SELECT 字段列表 FROM 表名列表 WHERE 条件列表 GROUP BY 分组字段 HAVING 分组之后的条件 ORDER BY 排序 LIMIT 分页限定




```

