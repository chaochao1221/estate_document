#用户-登录

####URL：/v1/user/login

##请求方式：POST

##是否需要授权
否

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| email  | true | char | 邮箱 |
| password | true | char | 密码 |
| group_id | true | int | 分组id(1:本部 2:中国 3:日本) |

##响应:
| 名称  | 类型  | 说明 |
|:------- |:----:| --------:|
| code    | int  |  错误代码 |
| msg     | char |  返回信息 |

###JSON示例:
```
// Status Codes 201 成功返回
{
    "data":{
    	"Authorization": "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX3R5cGUiOiJhZG1pbiIsInVzZXJfaWQiOjUsImdyb3VwX2lkIjoxLCJleHAiOjE0NzcwMzEwMjh9.FIuwxgYO52Zjw5up5h2q71cs3vdEiSsd63g7GUEE1-8"
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