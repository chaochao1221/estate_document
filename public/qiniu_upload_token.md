#公用-七牛token

####URL：/v1/public/qiniu_upload_token

##请求方式：GET

##是否需要授权
是

关于授权，参见 [接口规范][1]

##参数:
| 名称 | 必选 | 类型 | 说明 |
|:------:|:----:|:----:|:------|
| type | false | char | 上传资源的类型 img:图片 file:非图片文件(Word/Excel/PowerPoint/PDF) audio:音频 video:视频 |
| key  | false | char | 上传资源的key 例: img/2016/03/03/104115-9726.gif |

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
        "uptoken": "4D-Ef42EOmhLlhdGt2HbGTaWlbvWPrEFgzLv3HiD:SFfkJYwE6o_HACEMG0-N0Yk_i1o=:eyJzY29wZSI6ImZpbGVzOi96eTAwMS8yMDE2LzAzLzA4Lzk5OTk5OS0yMjIyLmpwZyIsImRlYWRsaW5lIjoxNDU3NDM2NzkzfQ=="
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