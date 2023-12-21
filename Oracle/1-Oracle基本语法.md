# 一、基本SQL-SELECT语句

### 1.空值运算

##### 1.1 概述

空值不是0，且查询时不参与运算

### 2.连接符

##### 2.1 概述

把**列与列**或**列与字符**连接在一起

##### 2.2 示例

```sql
SELECT last_name||job_id AS "Employees" FROM employees;
```

**注意事项**

日期和字符只能在单引号中出现

### 3.测试问题与答案

- 对于日期型数据, 做 *, / 运算不合法

- 包含空值的数学表达式的值都为空值

- 别名使用双引号!

- oracle 中连接字符串使用 "||", 而不是 java 中的 "+"

- 日期和字符只能在单引号中出现
- distinct 关键字, 以下语法错误`select last_name, distinct department_id from employees`