#本部中介-客户管理-编辑

####URL：/v1/base/customer_manage/edit

##请求方式：POST

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| id   | true | int | 推荐id |
| name | true | char| 姓名 |
| sex  | true | int | 性别（0:女 1:男）|
| wechat | true | char | 微信号 |
| is_butt | true | int | 是否对接（1:是 0:否）|
| is_to_japan | true | int | 是否赴日（1:是 0:否）|
| is_agree | true | int | 是否成约（1:是 0:否）|
| is_pay  | true | int | 是否付款（1:是 0:否）|
| is_loan | true | int | 是否贷款（1:是 0:否）|
| estate_code | true | char | 房源编号 |
| price | true | char | 实际成交价 |
| telephone | false | char | 手机号 |
| loan_time_1 | false | char | 仮審査 |
| loan_time_2 | false | char | 契約 |
| loan_time_3 | false | char | 本審査 |
| loan_time_4 | false | char | 金消 |
| loan_time_5 | false | char | 適合 |
| loan_time_6 | false | char | 決済 |
| remark | false | char | 备注 |

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