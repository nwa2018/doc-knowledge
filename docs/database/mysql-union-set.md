# mysql获取两个集合的交集/差集/并集

[【mysql】mysql获取两个集合的交集/差集/并集](https://blog.csdn.net/ColdFireMan/article/details/73284641)

`union`可以自动去除重复的内容,得到不重复的结果集

### 差集

查询非技术不员工的`id`, `code`, `name`
``` sql
SELECT a.* FROM(
    SELECT id,code,name FROM test_emp
    UNION ALL
    SELECT id,code,name FROM test_emp WHERE dept='JSB'
)a GROUP BY a.id HAVING COUNT(a.id)=1
```

### 交集
下面的`sql`的意思是找到所有技术部年龄大于`25`的员工

``` sql
SELECT a.* FROM(
    SELECT id,code,name FROM test_emp WHERE age>25
    UNION ALL
    SELECT id,code,name FROM test_emp WHERE dept='JSB'
)a GROUP BY a.id HAVING COUNT(a.id)=2
```

### 并集
下面的sql的意思是找到所有技术部的员工和年龄大于30的员工
``` sql
SELECT a.* FROM(
    SELECT id,code,name FROM test_emp WHERE age>25
    UNION
    SELECT id,code,name FROM test_emp WHERE dept='JSB'
)a
```
