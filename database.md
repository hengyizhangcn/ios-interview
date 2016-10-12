# database-review
数据库知识点记录

#1.常见的数据库有哪些
MySQL 轻量级，源码开放,  
SqlServer 微软公司,   
Oracle 甲骨文公司  
DB2 IBM  
Sybase  
Sqlite  

##分部式数据库:
(NoSQL, 非结构化)  
MongoDB, HBase(和Hadoop关联), Cassandra(Facebook)  
数据分片类型：水平分片，垂直分片，导出分片，混合分片  
    分片条件：完备性条件，可重构条件，不相交条件  
数据分配方式：集中式，分割式，全复制式，混合式  
  
另：Redis，用于高速内存缓存数据应用  
  
#2.数据库语言  
##DDL   
create, alter, drop  
eg.操作数据库  
create database class;  
drop database class;  
  
eg. 操作表  
以mysql为例  
create table person(creidtId varchar(18) primary key, name text, age int, height int)  
  
alter table person modify column height float  
alter table person drop column height  
alter table person add column height int  
  
drop table person  
  
##DQL
select  
eg.  
select * from person where age < 18  
  
##DML
insert, update, delete  
eg.  
insert person values("12233219800512238X", "Michael", 15, 178)  
update person set age = 20 where name = "Michael"  
delete from person where creidtID = "12233219800512238X"  
  
##DCL
grant, revoke，用于操作数据库  
eg.  
grant select/insert/update/delete/create/alter/drop/index/create view/references on person to users@micheal    
revoke update on person from users@micheal  
  
###连接
###聚合
###关键字查询
##view 视图
create view my_view as name, age on person  
alter view my_view ...  
##procedure 存储过程
create procedure getNum   
(in limit_age int,  
out num int)     
select count(*) num from person where age < limit_age;    
使用  
call getNum(25, @num);  
查询  
select * from mysql.proc where db = 'test' and `type` = 'PROCEDURE';  
##index 索引
##trigger 触发器（特殊的存储过程）  
delimiter ||   
drop trigger if exists my_trigger||  
create trigger my_trigger  
after insert on person  
for each row  
begin  
if new.age > 30 then  
delete from person where creidtId = new.creidtId;  
end if;  
end||  
delimiter;||  
使用  
insert into person value("1234567", "lili", 34, 188);||  
会报错如下  
Can't update table 'person' in stored function/trigger because it is already used by statement which invoked this stored function/trigger.  
原因是age不符合规则  
##

#设计范式
##第一范式 1NF
原子性，字段不能再分
##第二范式 2NF
惟一性，一列说明一个事物，数据列中无重复数据
##第三范式 3NF
不存在传递依赖，每列直接依赖主键
##       BCNF
##第四范式 4NF
##第五范式 5NF



Markdown: http://www.appinn.com/markdown/#p
