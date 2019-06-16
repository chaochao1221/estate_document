#公司-房源详情

####URL：/v1/public/estate_detail

##请求方式：GET

##是否需要授权
否

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
        "estate_name": "东京都中野公寓",  // 房源名称
        "estate_code": "201807230666",  // 房源编码
        "price": "8580.10",             // 价格（日元）
        "price_rmb": "492.10",          // 价格（人名币）
        "points": 3,                    // 点数
        "huxing": "1LDK",               // 户型
        "huxing_alias": "1室2厅",        // 户型别名
        "measure_area": "95.31",        // 面积
        "housing_type": 1,              // 房屋类型（1:普通公寓 2:公寓 3:一户建 4:别墅 5:民宿 6:简易旅馆 0:其他）
        "land_rights": 1,               // 土地权利（1:土地所有权 2:土地租借权）
        "building_time": "1998年6月",    // 建筑年月
        "floor": 6,                     // 楼层
        "total_floor": 19,              // 总楼层
        "building_structure": 1,        // 建筑结构（1:钢筋混泥土 2:钢结构 3:木结构）
        "orientation": "东",            // 朝向
        "repair_fee": "15000.10",       // 修缮费
        "state": 1,                     // 现状（1:空置 2:出租中 3:运营中）
        "rent": "60000.10",             // 租金
        "return_rate": "3.5",           // 回报率
        "manage_fee": "29540.10",       // 管理费
        "region_id": 1,                 // 地区id
        "area_id": 2,                   // 区域id
        "region_name": "东京都",         // 地区名称
        "area_name": "千代田区",         // 区域名称
        "traffic": [                    // 交通
            {
                "traffic_id": 1,            // 线路id
                "traffic_name": "线路1",     // 线路名称
                "station_id": 2,             // 站点id
                "station_name": "赤坂站",    // 站点名称
                "time": "12"                // 时间（分钟）
            },
            ...
        ],
        "address": "",                  // 地址
        "longitude": "",                // 经度
        "latitude": "",                 // 纬度
        "picture": "",                  // 图片地址（多张用逗号分割）
        "title": "",                    // 标题
        "land_area": "",                // 土地面积
        "building_cover": 60,           // 建筑覆盖率
        "plot_ratio": 240,              // 容积率
        "road": "",                     // 门前道路
        "road_width": "",               // 路宽
        "area_uses": 1,                 // 区域用途（1:第1種低層住居専用地域 2:第2種低層住居専用地域 3:第1種中高層住居専用地域 4:第2種中高層住居専用地域 5:第1種住居地域 6:第2種住居地域 7:準住居地域 8:田园住居地域 9:近临商業地域 10:商業地域 11:準工業地域 12:工業地域 13:工業専用地域）
        "exist_elevotar": 1,            // 是否存在电梯（1:是 0:否）
        "manage_style": 1,              // 管理方式（1:自主管理 2:巡回管理 3:长勤管理）
        "exist_parking": 1,             // 是否存在停车场（1:是 0:否）
        "visit_number": 1,              // 访问量
        "balcony_measure": "",          // 阳台面积
        "households": 20,               // 总户数
        "item_type": 1                  // 物件类型（1:公寓 2:土地 3:别墅 4:整栋物件）
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