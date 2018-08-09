#本部中介-客户管理-列表

####URL：/v1/base/customer_manage/list

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| notice_id | false | int | 我的通知id（从我的通知点击过来必传，其他不传）|
| keyword  | false | char| 搜索关键字 |
| user_id  | false | int | 本部销售用户id，不传默认显示全部 |
| company_id| false | int | 中国中介公司id，不传默认显示全部 |
| is_butt | false | char | 是否对接（"1":是 "0":否 不选传空字符串）|
| is_to_japan | false | char | 是否赴日（"1":是 "0":否 不选传空字符串）|
| is_agree | false | char | 是否成约（"1":是 "0":否 不选传空字符串）|
| is_pay | false | char | 是否付款（"1":是 "0":否 不选传空字符串）|
| is_loan | false | char | 是否贷款（"1":是 "0":否 不选传空字符串）|
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
                "id": 1,                    // 推荐id
                "name": "张亮",              // 姓名
                "sex": 1,                   // 性别（0:女 1:男）
                "wechat": "zl",             // 微信号
                "add_time": "2018/07/31",   // 添加时间
                "is_butt": 0,               // 是否对接（1:是 0:否）
                "is_to_japan": 0,           // 是否赴日（1:是 0:否）
                "is_agree": 0,              // 是否成约（1:是 0:否）
                "is_pay": 0,                // 是否付款（1:是 0:否）
                "is_loan": 0                // 是否贷款（1:是 0:否）
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