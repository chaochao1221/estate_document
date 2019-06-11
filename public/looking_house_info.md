#公用-找房(找房)

####URL：/v1/public/looking_house_info

##请求方式：GET

##是否需要授权
否

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| region_id | false | int | 地区id |
| budget | false | char | 预算（eg: 100-200 0-*）|
| room_number | false | char | 房型（1:一室 2:二室 3:三室 4:四室 5:五室 6:五室以上），多种房型用逗号拼接 |
| foot_time | false | int | 徒步时间（1:无限制 2:步行3分钟以内 2:5分钟内）|

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
        "function_id": 1,           // 功能id（0:找房 1:区域 2:预算 3:房型 4:徒步时间）
        "function_type": 0,         // 功能类型（0:底部显示；1:弹框显示）
        "message": [
            {
                "message_type": 0,      // 消息类型（0:普通消息 1:房源消息）
                "message_name": "",     // 消息名称
                "estate_id: 1,          // 房源id
                "estate_name": "",      // 房源名称
                "picture": "",          // 图片地址（多张用逗号分割）
                "price": "858",         // 价格（万元）
                "return_rate": "7.1",   // 回报率
                "huxing_alias": "1室2厅",// 户型别名
                "measure_area": "95.31",// 面积
                "floor": 6              // 楼层
            },
            ...
        ],
        "region": [
            {
                "region_id": 1,         // 地区id
                "region_name": "东京都"  // 地区名称
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