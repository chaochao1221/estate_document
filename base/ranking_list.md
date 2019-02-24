#本部中介-排行榜列表

####URL：/v1/base/ranking_list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| add_time | true | char | 时间 |

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
        		"name": "张三丰",        // 姓名
                "number": 2,            // 成交单数
                "total_price": "28900"  // 实际成交价（单位：万日元）
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