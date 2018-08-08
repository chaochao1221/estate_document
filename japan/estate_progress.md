#日本中介-房源进展

####URL：/v1/japan/estate_progress

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| status  | false | int | 房源状态（1:发布中 2:已下架 3:已成交），不传默认显示全部 |
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
                "id": 1,                        // 房源进展id
                "estate_code": "201807230666",  // 房源编码
                "housing_type": 1,              // 房屋类型（1:普通公寓 2:公寓 3:一户建 4:别墅 5:民宿 6:简易旅馆 0:其他）
                "region_name": "东京都-中野",     // 地区名称
                "measure_area": "95.31",        // 面积
                "price": "8580.0",              // 价格（日元）
                "customer_number": 2,           // 意向客户数量
                "status": 1,                    // 房源状态（1:发布中 2:已下架 3:已成交）
                "add_time": "2018/07/28"        // 添加时间
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