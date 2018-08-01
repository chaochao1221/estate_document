#本部中介-中国中介管理-列表

####URL：/v1/base/china_manage/list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| keyword  | false | char| 搜索关键字 |
| region_id| false | int | 地区id，不传默认显示全部 |
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
                "id": 1,                    // 中介公司id
                "company_name": "安居客",    // 中介公司名称
                "user_name": "张三",         // 联系人姓名
                "telephone": "90123467",    // 联系电话
                "add_time": "2018-11-10"    // 添加时间
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