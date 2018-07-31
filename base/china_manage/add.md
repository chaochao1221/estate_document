#本部中介-中国中介管理-添加/编辑

####URL：/v1/base/china_manage/add

##请求方式：POST

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| id | false | int | 中介公司id（添加不传，编辑必传）|
| region_id | true | int | 地区id |
| company_name | true | char | 中介公司名称 |
| address | true | char | 中介公司地址 |
| user_name | true | char | 联系人姓名 |
| telephone | true | char | 联系电话 |
| fax | true | char | 传真 |
| email | true | char | 邮箱 |
| password | false | char | 密码 |

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