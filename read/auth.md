#必读-验证

##请求Header:
| 名称 | 必选 | 类型 | 说明 |
|:-------------:|:----:|:----:|:----------|
| Authorization | true | char | Signature |

##说明:
简要流程：
```
	1.用户使用用户名和密码请求登录；
	2.服务端验证成功后会签发一个Authorization（注意有时效），再把这个Authorization发送给客户端；
	3.客户端每次向服务端请求资源的时候需要带着服务端签发的Authorization；
	4.服务端收到请求，验证客户端的Authorization，成功就向客户端返回请求的数据。
```
HEADER:
```
{
    "typ": "JWT",
    "alg": "HS256"
}
```
PAYLOAD:
```
{
    "application": "estate" // 应用
    "group_id": 1,          // 公司id(1:本部 2:中国 3:日本)
    "user_type": 1,         // 用户类型(1:主管 0:普通销售)
    "user_id": 5,           // 用户id
    "exp": 1477031028       // 过期时间(目前为签发起24小时)
}
```
Signature示例:
```
Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyX3R5cGUiOiJhZG1pbiIsInVzZXJfaWQiOjUsImdyb3VwX2lkIjoxLCJleHAiOjE0NzcwMzEwMjh9.FIuwxgYO52Zjw5up5h2q71cs3vdEiSsd63g7GUEE1-8
```