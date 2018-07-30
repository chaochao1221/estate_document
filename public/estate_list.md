#公用-房源列表

####URL：/v1/public/estate_list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| estate_code | false | char | 房源编码 |
| listorder | false | int | 排序方式（0:最新 1:面积 2:价格） |
| screen_json | false | int | 筛选json，参见以下示例（需严格按照示例json字段类型传参）： |
| per_page | false | int | 每页显示数量（默认为10）|
| last_id  | false | int | 当前页面最后一条数据id（第一次进来默认传0） |

##响应:
| 名称  | 类型  | 说明 |
|:------- |:----:| --------:|
| code    | int  |  错误代码 |
| msg     | char |  返回信息 |

###JSON示例:
```
screen_json={
    "region_id": 1          // 地区id 
    "area_id": 2,           // 区域id 
    "price_min": "200",     // 最低售价
    "price_max": "400",     // 最高售价
    "area_min": "40.15",    // 最小面积
    "area_max": "50.15",    // 最大面积
    "room_number": 1,       // 房间数量（1:一室 2:二室 3:三室 4:四室 5:五室 6:五室以上）
    "housing_type": 1,      // 房屋类型（1:普通公寓 2:公寓 3:一户建 4:别墅 5:民宿 6:简易旅馆 0:其他）
    "building_time": 1,     // 房龄（1:2年一下 2:2-5年 3:5-10年 4:10年以上）
    "orientation": 1,       // 朝向（1:东 2:南 3:西 4:北 5:南北 6:东西 7:东南 8:西南 9:东北 10:西北）
    "floor": 1,             // 楼层（1:6层以下 2:6-12层 3:12层以上）
    "building_structure": 1 // 建筑结构（1:钢筋混泥土 2:钢结构 3:木结构）
}

// Status Codes 200 成功返回
{
    "data": {
        "list": [
            {
                "estate_id": 1,                 // 房源id
                "region_name": "东京都",         // 地区名称
                "area_name": "中野",             // 区域名称
                "room_number": 2,               // 房间数量
                "exist_living_room": 1,         // 是否存咋客厅（1:是 0:否）
                "exist_dining_room": 1,         // 是否存在饭厅（1:是 0:否）
                "exist_kitchen": 1,             // 是否存咋厨房（1:是 0:否）
                "measure_area": "95.31",        // 面积
                "housing_type": 1,              // 房屋类型（1:普通公寓 2:公寓 3:一户建 4:别墅 5:民宿 6:简易旅馆 0:其他）
                "price": "8580.0",              // 价格（日元）
                "price_rmb": "492"              // 价格（人名币）
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