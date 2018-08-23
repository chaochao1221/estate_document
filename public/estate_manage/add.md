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
| huxing | true | char | 户型 |
| measure_area | true | string | 面积 |
| housing_type | true | int | 房屋类型（1:普通公寓 2:公寓 3:一户建 4:别墅 5:民宿 6:简易旅馆 0:其他）|
| floor | true | int | 楼层 |
| total_floor | true | int | 总楼层 |
| building_time | true | string | 建筑年月 |
| building_structure | true | int | 建筑结构（1:钢筋混泥土 2:钢结构 3:木结构）|
| land_rights | true | int | 土地权利（1:土地所有权 2:土地租借权）|
| orientation | true | string | 朝向 |
| state | true | int | 现状（1:空置 2:出租中 3:运营中）|
| rent | true | char | 租金 |
| return_rate | true | string | 回报率 |
| repair_fee | true | char | 修缮费 |
| manage_fee | true | char | 管理费 |
| region_id | true | int | 地区id |
| traffic | true | char | 交通 |
| address | true | char | 地址 |
| picture | true | char | 图片 |

##响应:
| 名称  | 类型  | 说明 |
|:------- |:----:| --------:|
| code    | int  |  错误代码 |
| msg     | char |  返回信息 |

###JSON示例:
```
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