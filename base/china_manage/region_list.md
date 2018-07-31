#本部中介-中国中介管理-地区列表

####URL：/v1/base/china_manage/region_list

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
                "region_id": 1,          // 地区id
                "region_name": "江苏",    // 地区名称
                "mark": 1                // 标记该地区下是否存在公司（1:存在 0:不存在）
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