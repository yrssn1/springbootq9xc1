# springboot068桂林旅游景点导游平台

## 简介

本代码仅供学习参考使用

加QQ(**3055269939**)免费获取项目和论文

## 主要内容

### 数据库设计表

桂林旅游景点导游平台需要后台数据库，下面介绍数据库中的各个表的详细信息：

 

 

表4.1 景点信息评论表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| refid     | bigint(20)   | 否   |                   | 关联表id |
| userid    | bigint(20)   | 否   |                   | 用户id   |
| nickname  | varchar(200) | 是   | NULL              | 用户名   |
| content   | longtext     | 否   |                   | 评论内容 |
| reply     | longtext     | 是   | NULL              | 回复内容 |

表4.2 线路推荐评论表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| refid     | bigint(20)   | 否   |                   | 关联表id |
| userid    | bigint(20)   | 否   |                   | 用户id   |
| nickname  | varchar(200) | 是   | NULL              | 用户名   |
| content   | longtext     | 否   |                   | 评论内容 |
| reply     | longtext     | 是   | NULL              | 回复内容 |

表4.3 论坛交流

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| title     | varchar(200) | 是   | NULL              | 帖子标题 |
| content   | longtext     | 否   |                   | 帖子内容 |
| parentid  | bigint(20)   | 是   | NULL              | 父节点id |
| userid    | bigint(20)   | 否   |                   | 用户id   |
| username  | varchar(200) | 是   | NULL              | 用户名   |
| isdone    | varchar(200) | 是   | NULL              | 状态     |

表4.4 景点类型

| 字段            | 类型         | 空   | 默认              | 注释     |
| --------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)       | bigint(20)   | 否   |                   | 主键     |
| addtime         | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| jingdianleixing | varchar(200) | 是   | NULL              | 景点类型 |

表4.5 景点信息

| 字段              | 类型         | 空   | 默认              | 注释     |
| ----------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)         | bigint(20)   | 否   |                   | 主键     |
| addtime           | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| jingdianmingcheng | varchar(200) | 是   | NULL              | 景点名称 |
| jingdianleixing   | varchar(200) | 是   | NULL              | 景点类型 |
| jingdiantupian    | varchar(200) | 是   | NULL              | 景点图片 |
| zixundianhua      | varchar(200) | 是   | NULL              | 咨询电话 |
| jingdianxiangqing | longtext     | 是   | NULL              | 景点详情 |
| thumbsupnum       | int(11)      | 是   | 0                 | 赞       |
| crazilynum        | int(11)      | 是   | 0                 | 踩       |

表4.6 新闻资讯

| 字段         | 类型         | 空   | 默认              | 注释     |
| ------------ | ------------ | ---- | ----------------- | -------- |
| id (主键)    | bigint(20)   | 否   |                   | 主键     |
| addtime      | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| title        | varchar(200) | 否   |                   | 标题     |
| introduction | longtext     | 是   | NULL              | 简介     |
| picture      | varchar(200) | 否   |                   | 图片     |
| content      | longtext     | 否   |                   | 内容     |

表4.7 收藏表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| userid    | bigint(20)   | 否   |                   | 用户id   |
| refid     | bigint(20)   | 是   | NULL              | 收藏id   |
| tablename | varchar(200) | 是   | NULL              | 表名     |
| name      | varchar(200) | 否   |                   | 收藏名称 |
| picture   | varchar(200) | 否   |                   | 收藏图片 |

表4.8 管理员表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| username  | varchar(100) | 否   |                   | 用户名   |
| password  | varchar(100) | 否   |                   | 密码     |
| role      | varchar(100) | 是   | 管理员            | 角色     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 新增时间 |

表4.9 线路推荐

| 字段            | 类型         | 空   | 默认              | 注释     |
| --------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)       | bigint(20)   | 否   |                   | 主键     |
| addtime         | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| xianlubianhao   | varchar(200) | 否   |                   | 线路编号 |
| biaoti          | varchar(200) | 是   | NULL              | 标题     |
| peitu           | varchar(200) | 是   | NULL              | 配图     |
| chufadi         | varchar(200) | 是   | NULL              | 出发地   |
| mudedi          | varchar(200) | 是   | NULL              | 目的地   |
| yudingshuliang  | int(11)      | 是   | NULL              | 预订数量 |
| yudingjiage     | int(11)      | 是   | NULL              | 预订价格 |
| xianluxiangqing | longtext     | 是   | NULL              | 线路详情 |
| thumbsupnum     | int(11)      | 是   | 0                 | 赞       |
| crazilynum      | int(11)      | 是   | 0                 | 踩       |

表4.10 用户

| 字段         | 类型         | 空   | 默认              | 注释     |
| ------------ | ------------ | ---- | ----------------- | -------- |
| id (主键)    | bigint(20)   | 否   |                   | 主键     |
| addtime      | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| yonghuming   | varchar(200) | 否   |                   | 用户名   |
| mima         | varchar(200) | 否   |                   | 密码     |
| xingming     | varchar(200) | 否   |                   | 姓名     |
| xingbie      | varchar(200) | 是   | NULL              | 性别     |
| shouji       | varchar(200) | 是   | NULL              | 手机     |
| youxiang     | varchar(200) | 是   | NULL              | 邮箱     |
| shenfenzheng | varchar(200) | 是   | NULL              | 身份证   |
| zhaopian     | varchar(200) | 是   | NULL              | 照片     |

表4.11 预订信息

| 字段           | 类型         | 空   | 默认              | 注释     |
| -------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)      | bigint(20)   | 否   |                   | 主键     |
| addtime        | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| yudingdanhao   | varchar(200) | 否   |                   | 预订单号 |
| xianlubianhao  | varchar(200) | 是   | NULL              | 线路编号 |
| biaoti         | varchar(200) | 是   | NULL              | 标题     |
| peitu          | varchar(200) | 是   | NULL              | 配图     |
| chufadi        | varchar(200) | 是   | NULL              | 出发地   |
| mudedi         | varchar(200) | 是   | NULL              | 目的地   |
| yudingshuliang | int(11)      | 是   | NULL              | 预订数量 |
| yudingjiage    | int(11)      | 是   | NULL              | 预定价格 |
| zongjine       | int(11)      | 是   | NULL              | 总金额   |
| yonghuming     | varchar(200) | 是   | NULL              | 用户名   |
| xingming       | varchar(200) | 是   | NULL              | 姓名     |
| shenfenzheng   | varchar(200) | 是   | NULL              | 身份证   |
| yudingshijian  | datetime     | 是   | NULL              | 预定时间 |
| beizhu         | varchar(200) | 是   | NULL              | 备注     |
| ispay          | varchar(200) | 是   | 未支付            | 是否支付 |