#公用-热门地区列表

####URL：/v1/public/hot_area_list

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
                "area_id": 1,
                "area_name": "东京",
                "estate_number": 1056
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