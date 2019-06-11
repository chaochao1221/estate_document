#公用-找房(购房知识)

####URL：/v1/public/looking_house

##请求方式：GET

##是否需要授权
否

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| function_id | true | int | 功能id（0:首页 1:购房知识） |
| function_type | true | int | 功能分类（1:同类问题 2:重选分类）|

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
        "function_type": 0,         // 功能类型（0:底部显示；1:弹框显示）
        "message_name": ["", ""],   // 消息名称
        "show_type": 1,             // 显示类型（1:确定/取消 2:找房/电话咨询/更多问题）
        "function": [
            {
                "function_id": 1,           // 功能id
                "function_name": "找房",    // 功能名称
                "is_looking_house": 1       // 是否找房（1:是 0:否）
            },
            {
                "function_id": 2,
                "function_name": "购房知识",
                "is_looking_house": 0
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