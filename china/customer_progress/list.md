#中国中介-客户进展-列表

####URL：/v1/china/customer_progress/list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| keyword | false | char | 关键字检索 |
| status  | false | int | 状态（1:未对接 2:对接中 3:未赴日 4:已赴日 5:未成约 6:已成约 7:未付款 8:已付款 9:无贷款 10:已贷款），不传默认显示全部 |
| user_id | false | int | 销售用户id |

##响应:
| 名称  | 类型  | 说明 |
|:------- |:----:| --------:|
| code    | int  |  错误代码 |
| msg     | char |  返回信息 |

###JSON示例:
```
// Status Codes 200 成功返回
{
    "data": {
        "list": [
            {
                "id": 1,                    // 推荐id
                "estate_id": 1,             // 房产id
                "name": "丁超",              // 姓名
                "wechat": "dingchao",       // 微信号
                "sex": 1,                   // 性别
                "status": 1,                // 状态（1:未对接 2:对接中 3:未赴日 4:已赴日 5:未成约 6:已成约 7:未付款 8:已付款 9:无贷款 10:已贷款）
                "add_time": "2018-07-28"    // 添加时间
            },
            ...
        ]
    },
    "code": 0,
    "msg": "success"
}
// Status Codes 400 失败返回
{
    "code": 1010,
    "msg": "失败原因"
}
```
[1]: ../read/auth.html