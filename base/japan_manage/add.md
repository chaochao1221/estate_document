#本部中介-日本中介管理-添加/编辑

####URL：/v1/base/japan_manage/add

##请求方式：POST

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| id | false | int | 会社id（添加不传，编辑必传）|
| company_name | true | char | 会社名称 |
| address | true | char | 会社地址 |
| user_id | false | int | 联系人姓名id（添加不传，编辑必传）|
| user_name | true | char | 联系人姓名 |
| telephone | true | char | 联系电话 |
| fax | true | char | 传真 |
| email | true | char | 邮箱 |
| password | false | char | 密码（添加必传，编辑非必传）|
| expiry_date | true | char | 过期时间 |

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