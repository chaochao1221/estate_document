#必读-状态码

##说明:

服务器向用户返回的状态码和提示信息：

    200 OK - [GET]：服务器成功返回用户请求的数据，该操作是幂等的。
    201 CREATED - [POST/PUT/PATCH]：用户新建或修改数据成功。
    400 INVALID REQUEST - [GET/POST/PUT/PATCH]：用户发出的请求有错误，服务器没有进行新建或修改数据的操作，该操作是幂等的。
    401 Unauthorized - [*]：表示用户没有权限。
    404 NOT FOUND - [*]：路由不存在。
