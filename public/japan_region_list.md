#公用-日本地区列表

####URL：/v1/public/japan_region_list

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
        "region": [
            {
                "region_id": 1,
                "region_name": "东京",
                "area": [
                    {
                        "area_id": 2,
                        "area_name": "千代田区"
                    },
                    ...
                ]
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