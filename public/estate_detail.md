#公司-房源详情

####URL：/v1/public/estate_detail

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| estate_id | true | int | 房源id |

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
        "estate_id": 1,                 // 房源id
        "estate_code": "201807230666",  // 房源编码
        "region_name": "东京都",         // 地区名称
        "area_name": "中野",             // 区域名称
        "room_number": 2,               // 房间数量
        "exist_living_room": 1,         // 是否存咋客厅（1:是 0:否）
        "exist_dining_room": 1,         // 是否存在饭厅（1:是 0:否）
        "exist_kitchen": 1,             // 是否存咋厨房（1:是 0:否）
        "measure_area": "95.31",        // 面积
        "housing_type": 1,              // 房屋类型（1:普通公寓 2:公寓 3:一户建 4:别墅 5:民宿 6:简易旅馆 0:其他）
        "price": "8580.0",              // 价格（日元）
        "price_rmb": "492",             // 价格（人名币）
        "land_rights": 1,               // 土地权利（1:土地所有权 2:土地租借权）
        "building_time": "1998年6月",    // 建筑年月
        "floor": 6,                     // 楼层
        "total_floor": 19,              // 总楼层
        "building_structure": 1,        // 建筑结构（1:钢筋混泥土 2:钢结构 3:木结构）
        "orientation": 1,               // 朝向（1:东 2:南 3:西 4:北 5:南北 6:东西 7:东南 8:西南 9:东北 10:西北）
        "repair_fee": 15000,            // 修缮费
        "state": 1,                     // 现状（1:空置 2:出租中 3:运营中）
        "rent": 60000,                  // 租金
        "return_rate": "3.5",           // 回报率
        "manage_fee": 29540             // 管理费
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