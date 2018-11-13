#本部中介-我的通知-列表

####URL：/v1/base/notify/list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| status | false  | int | 通知状态（1:未读 2:已读 0:全部 默认0）|
| per_page | false | int | 每页显示数量（默认为10）|
| last_id  | false | int | 当前页面最后一条数据id（第一次进来默认传0） |

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
        "unread_number": 10,                        // 未读数量
        "list": [
            {
                "id": 1,                            // 通知id
                "status": 1,                        // 通知状态（1:未读 2:已读
                "name": "收到新的推荐客户",            // 通知名称
                "add_time": "2018-08-05 09:00:01"   // 添加时间
            },
            {
                "id": 2,
                "status": 1,
                "name": "收到新的咨询客户",
                "add_time": "2018-08-05 09:00:00"
            },
            ...
        ],
        "pagenation": {
            "last_id": 31   // 本页最后一条数据id，如果为-1则表示当前页为最后一页
        }
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