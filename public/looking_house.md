#公用-找房

####URL：/v1/public/looking_house

##请求方式：GET

##是否需要授权
否

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| function_id | true | int | 功能id（0:首页 1:购房知识） |

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
        "message_type": 0,          // 消息类型（0:普通消息；1:房源消息）
        "message_name": ["", ""],   // 消息名称
        "exist_child": 1,           // 是否存在子层（1:是 0:否）
        "function": [
            {
                "function_id": 1,           // 功能id
                "function_name": "找房"     // 功能名称
            },
            {
                "function_id": 2,
                "function_name": "购房知识"
            }
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