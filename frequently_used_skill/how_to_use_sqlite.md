
# Mac下使用sqlite数据库

查看数据库 不存在时则创建

```
sqlite aa.db
```

查看当前数据库的所有表

```
.tables
```

退出数据库

```
.quit
```

设置数据显示样式

```
.mode list
.mode line 
.mode column
```

查看表结构

```
pragma table_info(tablename)
```

默认值为当前日期

```
create table test_table (a integer , b date default (date(‘now’)));
```

