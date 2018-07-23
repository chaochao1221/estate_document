#用户-信息

####URL：/v1/user/info

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
        "name": "丁超",                  // 用户姓名
        "email": "934234902@qq.com",    // 邮箱
        "is_notified": 0                // 是否通知（1:是 0:否）
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