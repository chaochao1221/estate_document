#公用-交通列表

####URL：/v1/public/traffic_list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| area_id | true | int | 地区id |

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
        "traffic": [
            {
                "traffic_id": 1,
                "traffic_name": "线路1",
                "station": [
                    {
                        "station_id": 2,
                        "station_name": "站点1"
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