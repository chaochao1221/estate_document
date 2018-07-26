#公用-销售管理-列表

####URL：/v1/public/sales_manage/list

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
        {
            "user_id": 1,                   // 用户id
            "name": "丁超",                  // 姓名
            "email": "934234902@qq.com",    // 邮箱
            "add_time": "2018-07-26"        // 添加时间
        },
        ...
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