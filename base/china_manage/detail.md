#本部中介-中国中介管理-详情

####URL：/v1/base/china_manage/detail

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| id | true | int | 中介公司id |

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
        "id": 1,                    // 中介公司id
        "region_id": 1,             // 地区id
        "region_name": "江苏",       // 地区名称
        "company_name": "中原集团",  // 中介公司名称
        "address": "东京都千代户",    // 中介公司地址
        "user_id": 1,               // 联系人id
        "user_name": "三井",         // 联系人姓名
        "telephone": "90123467",    // 联系电话
        "fax": "987654321",         // 传真
        "email": "sjs"              // 邮箱
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