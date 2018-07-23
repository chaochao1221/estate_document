#用户-修改密码

####URL：/v1/user/modify_password

##请求方式：POST

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| old_password | true | char | 原密码 |
| new_password | true | char | 新密码 |

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