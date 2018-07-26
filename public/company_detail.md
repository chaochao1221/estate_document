#公用-公司详情

####URL：/v1/public/company_detail

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
    "data":{
        "group_id": 1,                  // 分组id(1:本部 2:中国 3:日本)
        "user_id": 1,                   // 用户id
        "user_type": 1,                 // 用户类型（0:销售 1:主管）
        "company_name": "安居客",        // 公司名称
        "c_recommend_number": 253,      // 累计推荐客户数
        "c_deal_number": 11,            // 累计成交客户数
        "e_release_number": 55,         // 累计发布房源数
        "e_deal_number": 3,             // 累计成交房源数
        "expiry_date": "2019-01-09"     // 帐号有效期
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