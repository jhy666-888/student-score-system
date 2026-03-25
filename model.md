学生课表

\# 学生选课成绩系统表结构



\## 1. 学生表 student

| 字段名 | 数据类型 | 约束 | 说明 |

|----|----|----|----|

| student\_id | INT | PRIMARY KEY, NOT NULL | 学号 |

| name | VARCHAR(20) | NOT NULL | 姓名 |

| gender | CHAR(1) | NULL | 性别 |

| age | INT | NULL | 年龄 |



\## 2. 教师表 teacher

| 字段名 | 数据类型 | 约束 | 说明 |

|----|----|----|----|

| teacher\_id | INT | PRIMARY KEY, NOT NULL | 教师编号 |

| name | VARCHAR(20) | NOT NULL | 姓名 |

| subject | VARCHAR(30) | NOT NULL | 授课科目 |



\## 3. 课程表 course

| 字段名 | 数据类型 | 约束 | 说明 |

|----|----|----|----|

| course\_id | INT | PRIMARY KEY, NOT NULL | 课程号 |

| name | VARCHAR(30) | NOT NULL | 课程名 |

| credit | INT | NOT NULL | 学分 |



\## 4. 选课成绩表 score

| 字段名 | 数据类型 | 约束 | 说明 |

|----|----|----|----|

| id | INT | PRIMARY KEY, AUTO\_INCREMENT | 自增ID |

| student\_id | INT | NOT NULL | 学号 |

| course\_id | INT | NOT NULL | 课程号 |

| score | INT | NULL | 成绩 |



外键：

score.student\_id 关联 student.student\_id

score.course\_id 关联 course.course\_id

