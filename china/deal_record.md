#中国中介-成交记录

####URL：/v1/china/deal_record

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| deal_time | true | char | 成交时间 |
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
        "list": [
            {
                "tourists_name": "张家辉",       // 游客姓名
                "sex": 1,                       // 性别（1:男 0:女）
                "wechat": "",                   // 微信号
                "price": "8580",                // 价格（万日元）
                "commission": "50",             // 佣金（万日元）
                "recommend_name": "李征",       // 推荐人
                "deal_time": "2019-01-02 08:08" // 成交时间
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