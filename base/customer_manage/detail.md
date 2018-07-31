#本部中介-客户管理-详情

####URL：/v1/base/customer_manage/detail

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| id | true | int | 推荐id |

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
        "id": 1,                    // 推荐id
        "name": "张亮",              // 姓名
        "sex": 1,                   // 性别（0:女 1:男）
        "wechat": "zl",             // 微信号
        "is_butt": 0,               // 是否对接（1:是 0:否）
        "is_to_japan": 0,           // 是否赴日（1:是 0:否）
        "is_agree": 0,              // 是否成约（1:是 0:否）
        "is_pay": 0,                // 是否付款（1:是 0:否）
        "is_loan": 0,               // 是否贷款（1:是 0:否）
        "estate_code": "SN12345",   // 房源编号
        "price": 15000              // 实际成交价
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