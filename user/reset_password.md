#用户-重置密码

####URL：/v1/user/reset_password

##请求方式：POST

##是否需要授权
否

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| email | true | char | 邮箱 |

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