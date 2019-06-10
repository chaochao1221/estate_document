#公用-电话咨询

####URL：/v1/public/consult

##请求方式：GET

##是否需要授权
否

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
        "avatar": "",                   // 头像
        "company_name": "yak株式会社",   // 公司名称
        "name": "丁先生",                // 姓名
        "telephone": "",                // 电话
        "working_day": "",              // 工作日
        "rest_day": ""                  // 休息日
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