#本部中介-中介费用统计-详情

####URL：/v1/base/sales_profit/detail

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| id | true  | int | 销售用户id |

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
                "estate_id": 1,                 // 房源id
                "estate_code": "2018073098922", // 方便编号
                "estate_name": "东京都中野区公寓", // 房源名称
                "price": 65000,                 // 中介费
                "deal_time": "2018-07-30"       // 成交时间
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