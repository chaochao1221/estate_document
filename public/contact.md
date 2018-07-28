#公司-联系方式

####URL：/v1/public/contact

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| estate_id | true | int | 房源id |

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
        "company_name": "三井置业会社",   // 会社名称
        "adress": "东京都千代田区",       // 会社地址
        "user_name": "田中熊二",         // 联系人
        "telephone": "56890123",        // 联系电话
        "fax": "56890123",              // 传真
        "email": "ting5678@gmail.com"   // 联系邮箱
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