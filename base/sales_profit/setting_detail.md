#本部中介-中介费用统计-设置详情

####URL：/v1/base/sales_profit/setting_detail

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| estate_id | true  | int | 房源id |

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
        "price": 9800,              // 销售额
        "agency_fee": 648,          // 中介费
        "seller": { // 卖家
            "service_fee": 3,       // 手续费
            "fixed_fee": 60000,     // 固定费
            "excise_fee": "1.08"    // 消费税
        },
        "buyer": {  // 买家
            "service_fee": 3,
            "fixed_fee": 60000,
            "excise_fee": "1.08"
        }
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