#公用-销售管理-添加/编辑

####URL：/v1/public/sales_manage/add

##请求方式：POST

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| user_id | false | int | 用户id（新建不传，编辑必传） |
| name  | true | char | 姓名 |
| email | true | char | 邮箱 |
| password | false | char | 密码 |
| telephone | false | char | 手机号 |

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