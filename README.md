# springboot大学生竞赛管理系统

## 简介

本代码仅供学习参考使用

加QQ(**3055269939**)获取完整项目和论文

## 主要内容

### 数据库设计表

大学生竞赛管理系统需要后台数据库，下面介绍数据库中的各个表的详细信息：

 

 

表4.1 班级类型

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| leixing   | varchar(200) | 是   | NULL              | 类型     |

表4.2 教师

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| gonghao          | varchar(200) | 否   |                   | 工号     |
| mima             | varchar(200) | 否   |                   | 密码     |
| jiaoshixingming  | varchar(200) | 否   |                   | 教师姓名 |
| xingbie          | varchar(200) | 是   | NULL              | 性别     |
| xueyuanmingcheng | varchar(200) | 是   | NULL              | 学院名称 |
| zhicheng         | varchar(200) | 是   | NULL              | 职称     |
| shouji           | varchar(200) | 是   | NULL              | 手机     |
| youxiang         | varchar(200) | 是   | NULL              | 邮箱     |
| zhaopian         | varchar(200) | 是   | NULL              | 照片     |

表4.3 竞赛报名

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| gonghao          | varchar(200) | 是   | NULL              | 工号     |
| jiaoshixingming  | varchar(200) | 是   | NULL              | 教师姓名 |
| jingsaimingcheng | varchar(200) | 是   | NULL              | 竞赛名称 |
| jingsaileixing   | varchar(200) | 是   | NULL              | 竞赛类型 |
| cansaileixing    | varchar(200) | 是   | NULL              | 参赛类型 |
| cansairenyuan    | varchar(200) | 是   | NULL              | 参赛人员 |
| cansaizuopin     | varchar(200) | 是   | NULL              | 参赛作品 |
| cansaixuanyan    | longtext     | 是   | NULL              | 参赛宣言 |
| shenqingriqi     | date         | 是   | NULL              | 申请日期 |
| xuehao           | varchar(200) | 是   | NULL              | 学号     |
| xueshengxingming | varchar(200) | 是   | NULL              | 学生姓名 |
| sfsh             | varchar(200) | 是   | 否                | 是否审核 |
| shhf             | longtext     | 是   | NULL              | 审核回复 |
| ispay            | varchar(200) | 是   | 未支付            | 是否支付 |

表4.4 竞赛信息

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| jingsaimingcheng | varchar(200) | 是   | NULL              | 竞赛名称 |
| jingsaileixing   | varchar(200) | 是   | NULL              | 竞赛类型 |
| jingsaididian    | varchar(200) | 是   | NULL              | 竞赛地点 |
| jingsaiguize     | longtext     | 是   | NULL              | 竞赛规则 |
| jingsaijiangli   | longtext     | 是   | NULL              | 竞赛奖励 |
| jingsaishijian   | datetime     | 是   | NULL              | 竞赛时间 |
| moshi            | varchar(200) | 是   | NULL              | 模式     |
| fengmiantupian   | varchar(200) | 是   | NULL              | 封面图片 |
| gonghao          | varchar(200) | 是   | NULL              | 工号     |
| jiaoshixingming  | varchar(200) | 是   | NULL              | 教师姓名 |

表4.5 管理员表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| username  | varchar(100) | 否   |                   | 用户名   |
| password  | varchar(100) | 否   |                   | 密码     |
| role      | varchar(100) | 是   | 管理员            | 角色     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 新增时间 |

表4.6 学生

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| xuehao           | varchar(200) | 否   |                   | 学号     |
| mima             | varchar(200) | 否   |                   | 密码     |
| xueshengxingming | varchar(200) | 否   |                   | 学生姓名 |
| xingbie          | varchar(200) | 是   | NULL              | 性别     |
| xueyuanmingcheng | varchar(200) | 是   | NULL              | 学院名称 |
| banji            | varchar(200) | 是   | NULL              | 班级     |
| shouji           | varchar(200) | 是   | NULL              | 手机     |
| youxiang         | varchar(200) | 是   | NULL              | 邮箱     |
| zhaopian         | varchar(200) | 是   | NULL              | 照片     |

表4. 7作品打分

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| xuehao           | varchar(200) | 是   | NULL              | 学号     |
| xueshengxingming | varchar(200) | 是   | NULL              | 学生姓名 |
| jingsaimingcheng | varchar(200) | 是   | NULL              | 竞赛名称 |
| jingsaileixing   | varchar(200) | 是   | NULL              | 竞赛类型 |
| zuopinpingfen    | int(11)      | 是   | NULL              | 作品评分 |
| pingjianeirong   | longtext     | 是   | NULL              | 评价内容 |
| pingjiashijian   | date         | 是   | NULL              | 评价时间 |
| gonghao          | varchar(200) | 是   | NULL              | 工号     |
| jiaoshixingming  | varchar(200) | 是   | NULL              | 教师姓名 |