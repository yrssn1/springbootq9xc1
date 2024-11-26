# springboot058美发门店管理系统

## 简介

本代码仅供学习参考使用

加QQ(**3055269939**)免费获取项目和论文

## 主要内容

### 数据库设计表

美发门店管理系统需要后台数据库，下面介绍数据库中的各个表的详细信息：

 

 

表4.1 产品购买

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| chanpinmingcheng | varchar(200) | 是   | NULL              | 产品名称 |
| chanpinleixing   | varchar(200) | 是   | NULL              | 产品类型 |
| chanpinshuliang  | int(11)      | 是   | NULL              | 产品数量 |
| chanpinshoujia   | int(11)      | 是   | NULL              | 产品售价 |
| zongjia          | varchar(200) | 是   | NULL              | 总价     |
| beizhu           | longtext     | 是   | NULL              | 备注     |
| shouhuodizhi     | varchar(200) | 是   | NULL              | 收货地址 |
| lianxidianhua    | varchar(200) | 是   | NULL              | 联系电话 |
| zhanghao         | varchar(200) | 是   | NULL              | 账号     |
| sfsh             | varchar(200) | 是   | 否                | 是否审核 |
| shhf             | longtext     | 是   | NULL              | 审核回复 |
| ispay            | varchar(200) | 是   | 未支付            | 是否支付 |

表4.2 产品库存

| 字段             | 类型         | 空   | 默认              | 注释         |
| ---------------- | ------------ | ---- | ----------------- | ------------ |
| id (主键)        | bigint(20)   | 否   |                   | 主键         |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间     |
| chanpinmingcheng | varchar(200) | 是   | NULL              | 产品名称     |
| chanpinleixing   | varchar(200) | 是   | NULL              | 产品类型     |
| gonghuochangjia  | varchar(200) | 是   | NULL              | 供货厂家     |
| chanpinjieshao   | longtext     | 是   | NULL              | 产品介绍     |
| chanpinshuliang  | int(11)      | 是   | NULL              | 产品数量     |
| chanpinshoujia   | int(11)      | 是   | NULL              | 产品售价     |
| xiangqing        | longtext     | 是   | NULL              | 详情         |
| tupian           | varchar(200) | 是   | NULL              | 图片         |
| thumbsupnum      | int(11)      | 是   | 0                 | 赞           |
| crazilynum       | int(11)      | 是   | 0                 | 踩           |
| clicktime        | datetime     | 是   | NULL              | 最近点击时间 |
| clicknum         | int(11)      | 是   | 0                 | 点击次数     |

表4.3 产品类型

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| leixing   | varchar(200) | 是   | NULL              | 类型     |

表4.4 产品入库

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| chanpinmingcheng | varchar(200) | 是   | NULL              | 产品名称 |
| chanpinleixing   | varchar(200) | 是   | NULL              | 产品类型 |
| gonghuochangjia  | varchar(200) | 是   | NULL              | 供货厂家 |
| chanpinshuliang  | int(11)      | 是   | NULL              | 产品数量 |
| chanpinjinjia    | int(11)      | 是   | NULL              | 产品进价 |
| beizhu           | longtext     | 是   | NULL              | 备注     |
| baifangweizhi    | varchar(200) | 是   | NULL              | 摆放位置 |
| rukuriqi         | date         | 是   | NULL              | 入库日期 |

表4.5 产品库存评论表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| refid     | bigint(20)   | 否   |                   | 关联表id |
| userid    | bigint(20)   | 否   |                   | 用户id   |
| nickname  | varchar(200) | 是   | NULL              | 用户名   |
| content   | longtext     | 否   |                   | 评论内容 |
| reply     | longtext     | 是   | NULL              | 回复内容 |

表4.6 会员充值

| 字段               | 类型         | 空   | 默认              | 注释       |
| ------------------ | ------------ | ---- | ----------------- | ---------- |
| id (主键)          | bigint(20)   | 否   |                   | 主键       |
| addtime            | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间   |
| huiyuankamingcheng | varchar(200) | 是   | NULL              | 会员卡名称 |
| huiyuankaleixing   | varchar(200) | 是   | NULL              | 会员卡类型 |
| jine               | int(11)      | 是   | NULL              | 金额       |
| chongzhifangshi    | varchar(200) | 是   | NULL              | 充值方式   |
| beizhu             | longtext     | 是   | NULL              | 备注       |
| lianxidianhua      | varchar(200) | 是   | NULL              | 联系电话   |
| zhanghao           | varchar(200) | 是   | NULL              | 账号       |
| sfsh               | varchar(200) | 是   | 否                | 是否审核   |
| shhf               | longtext     | 是   | NULL              | 审核回复   |
| ispay              | varchar(200) | 是   | 未支付            | 是否支付   |

表4.7 会员卡

| 字段               | 类型         | 空   | 默认              | 注释       |
| ------------------ | ------------ | ---- | ----------------- | ---------- |
| id (主键)          | bigint(20)   | 否   |                   | 主键       |
| addtime            | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间   |
| huiyuankamingcheng | varchar(200) | 是   | NULL              | 会员卡名称 |
| huiyuankaleixing   | varchar(200) | 是   | NULL              | 会员卡类型 |
| huiyuankajieshao   | longtext     | 是   | NULL              | 会员卡介绍 |
| huiyuankaqixian    | varchar(200) | 是   | NULL              | 会员卡期限 |
| jine               | int(11)      | 是   | NULL              | 金额       |
| faburiqi           | date         | 是   | NULL              | 发布日期   |
| tupian             | varchar(200) | 是   | NULL              | 图片       |

表4.8 美容项目

| 字段             | 类型         | 空   | 默认              | 注释         |
| ---------------- | ------------ | ---- | ----------------- | ------------ |
| id (主键)        | bigint(20)   | 否   |                   | 主键         |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间     |
| xiangmumingcheng | varchar(200) | 是   | NULL              | 项目名称     |
| xiangmuleixing   | varchar(200) | 是   | NULL              | 项目类型     |
| xiangmujieshao   | longtext     | 是   | NULL              | 项目介绍     |
| meironggongxiao  | longtext     | 是   | NULL              | 美容功效     |
| xiangmujine      | int(11)      | 是   | NULL              | 项目金额     |
| xiangqing        | longtext     | 是   | NULL              | 详情         |
| tupian           | varchar(200) | 是   | NULL              | 图片         |
| clicktime        | datetime     | 是   | NULL              | 最近点击时间 |
| clicknum         | int(11)      | 是   | 0                 | 点击次数     |

表4.9 收藏表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| userid    | bigint(20)   | 否   |                   | 用户id   |
| refid     | bigint(20)   | 是   | NULL              | 收藏id   |
| tablename | varchar(200) | 是   | NULL              | 表名     |
| name      | varchar(200) | 否   |                   | 收藏名称 |
| picture   | varchar(200) | 否   |                   | 收藏图片 |

表4.10 管理员表

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| username  | varchar(100) | 否   |                   | 用户名   |
| password  | varchar(100) | 否   |                   | 密码     |
| role      | varchar(100) | 是   | 管理员            | 角色     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 新增时间 |

表4.11 项目类型

| 字段      | 类型         | 空   | 默认              | 注释     |
| --------- | ------------ | ---- | ----------------- | -------- |
| id (主键) | bigint(20)   | 否   |                   | 主键     |
| addtime   | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| leixing   | varchar(200) | 是   | NULL              | 类型     |

表4.12 项目预定

| 字段             | 类型         | 空   | 默认              | 注释     |
| ---------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)        | bigint(20)   | 否   |                   | 主键     |
| addtime          | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| xiangmumingcheng | varchar(200) | 是   | NULL              | 项目名称 |
| xiangmuleixing   | varchar(200) | 是   | NULL              | 项目类型 |
| xiangmujine      | int(11)      | 是   | NULL              | 项目金额 |
| zhifufangshi     | varchar(200) | 是   | NULL              | 支付方式 |
| xiaofeiriqi      | date         | 是   | NULL              | 消费日期 |
| beizhu           | longtext     | 是   | NULL              | 备注     |
| lianxidianhua    | varchar(200) | 是   | NULL              | 联系电话 |
| zhanghao         | varchar(200) | 是   | NULL              | 账号     |
| sfsh             | varchar(200) | 是   | 否                | 是否审核 |
| shhf             | longtext     | 是   | NULL              | 审核回复 |
| ispay            | varchar(200) | 是   | 未支付            | 是否支付 |

表4.13 用户

| 字段          | 类型         | 空   | 默认              | 注释     |
| ------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)     | bigint(20)   | 否   |                   | 主键     |
| addtime       | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| zhanghao      | varchar(200) | 否   |                   | 账号     |
| mima          | varchar(200) | 否   |                   | 密码     |
| xingming      | varchar(200) | 否   |                   | 姓名     |
| xingbie       | varchar(200) | 是   | NULL              | 性别     |
| huiyuankahao  | varchar(200) | 是   | NULL              | 会员卡号 |
| shengri       | date         | 是   | NULL              | 生日     |
| lianxidianhua | varchar(200) | 是   | NULL              | 联系电话 |
| shenfenzheng  | varchar(200) | 是   | NULL              | 身份证   |

表4.14 余额查询

| 字段           | 类型         | 空   | 默认              | 注释     |
| -------------- | ------------ | ---- | ----------------- | -------- |
| id (主键)      | bigint(20)   | 否   |                   | 主键     |
| addtime        | timestamp    | 否   | CURRENT_TIMESTAMP | 创建时间 |
| zhanghao       | varchar(200) | 是   | NULL              | 账号     |
| huiyuankahao   | varchar(200) | 是   | NULL              | 会员卡号 |
| huiyuanleixing | varchar(200) | 是   | NULL              | 会员类型 |
| huiyuandengji  | int(11)      | 是   | NULL              | 会员等级 |
| banliriqi      | date         | 是   | NULL              | 办理日期 |
| shiyongshijian | varchar(200) | 是   | NULL              | 使用时间 |
| huiyuanyue     | int(11)      | 是   | NULL              | 会员余额 |