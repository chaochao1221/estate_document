#公用-房源管理-添加/编辑

####URL：/v1/public/estate_manage/add

##请求方式：POST

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| estate_id | false | int | 房源id（新建不传，编辑必传）|
| price | true | char | 价格 |
| points | true | int | 点数 |
| huxing | false | char | 户型 |
| measure_area | false | string | 面积 |
| housing_type | false | int | 房屋类型（1:普通公寓 2:公寓 3:一户建 4:别墅 5:民宿 6:简易旅馆 0:其他）|
| floor | false | int | 楼层 |
| total_floor | false | int | 总楼层 |
| building_time | false | string | 建筑年月 |
| building_structure | false | int | 建筑结构（1:钢筋混泥土 2:钢结构 3:木结构）|
| land_rights | false | int | 土地权利（1:土地所有权 2:土地租借权）|
| orientation | false | string | 朝向 |
| state | true | int | 现状（1:空置 2:出租中 3:运营中）|
| rent | false | char | 租金 |
| return_rate | false | string | 回报率 |
| repair_fee | false | char | 修缮费 |
| manage_fee | false | char | 管理费 |
| region_id | true | int | 地区id |
| area_id | true | int | 区域id |
| traffic | true | char | 交通json |
| address | true | char | 地址 |
| longitude | true | char | 经度 |
| latitude  | true | char | 纬度 |
| picture | true | char | 图片地址（多张用逗号分割）|
| title | false | char | 标题 |
| land_area | false | char | 土地面积 |
| building_cover | false | int | 建筑覆盖率 |
| plot_ratio | false | int | 容积率 |
| road | false | char | 门前道路 |
| road_width | false | char | 路宽 |
| area_uses | false | int | 区域用途（1:第1種低層住居専用地域 2:第2種低層住居専用地域 3:第1種中高層住居専用地域 4:第2種中高層住居専用地域 5:第1種住居地域 6:第2種住居地域 7:準住居地域 8:田园住居地域 9:近临商業地域 10:商業地域 11:準工業地域 12:工業地域 13:工業専用地域） |
| exist_elevotar | false | int | 是否存在电梯（1:是 0:否）|
| manage_style | false | int | 管理方式（1:自主管理 2:巡回管理 3:长勤管理）|
| exist_parking | false | int | 是否存在停车场（1:是 0:否）|
| balcony_measure | false | string | 阳台面积 |
| households | false | int | 总户数 |
| item_type | true | int | 物件类型（1:公寓 2:土地 3:别墅 4:整栋物件）|
| unit_price | false | string | 平米单价 |

##响应:
| 名称  | 类型  | 说明 |
|:------- |:----:| --------:|
| code    | int  |  错误代码 |
| msg     | char |  返回信息 |

###JSON示例:
```
traffic=[
	{
		"traffic_id": 1,            // 线路id
		"traffic_name": "线路1",     // 线路名称
		"station_id: 2,             // 站点id
		"station_name": "赤坂站",    // 站点名称
		"time": "12"				// 时间（分钟）
	}
]

// Status Codes 201 成功返回
{
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