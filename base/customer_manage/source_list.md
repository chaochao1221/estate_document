#本部中介-客户管理-来源列表

####URL：/v1/base/customer_manage/source_list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

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
                "company_id": 1,            // 中介公司id
                "company_name": "安居客"     // 中介公司名称
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