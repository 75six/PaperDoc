# 1.技师管理		

#### 1.1查询技师列表（分页）

接口名称： /user/queryUser 

请求方式：POST

请求报文：

```java
{
   
    "name" : "用户姓名（包含）",   
    "nickname" : "昵称（包含）",
    "sex" : "性别",
    "mobile" : "手机号（包含）",
    "idNumber" : "身份证号",
    "type" : "技师类型",
    "verified" : "是否实名认证",
    "postCode" : "岗位编号",
    "workTypeCode" : "工种编号",
    "pageNo": 0,
    "pageSize": 0,
    "sortBy": "排序方式"
   
}
```

返回报文：

```java
{
    "code":0,
	"msg":"成功",
    "data":{
        "userLists":[
            {
              {
                "id":0,    
                "accountId" : "通用账户id"  , 
                "name" : "用户姓名",   
                "nickname" : "昵称",
                "sex" : "性别",
                "mobile" : "手机号",
                "idNumber" : "身份证号",
                "qq" : "QQ号码",
                "wechat" : "微信号",
                "email" : "邮箱",
                "password" : "密码",   
                "school" : "毕业院校",
                "education" : "学历",
                "residentialAddress" : "居住地址",
                "type" : "技师类型",
                "source" : "注册渠道",
                "verified" : "是否实名认证",
                "seniority" : "工龄",
                "createdUser" : "创建人",
                "createdTime" : "创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "description" : "描述"    
              }，
               {
                "id":0,    
                "accountId" : "通用账户id"  , 
                "name" : "用户姓名",   
                "nickname" : "昵称",
                "sex" : "性别",
                "mobile" : "手机号",
                "idNumber" : "身份证号",
                "qq" : "QQ号码",
                "wechat" : "微信号",
                "email" : "邮箱",
                "password" : "密码",   
                "school" : "毕业院校",
                "education" : "学历",
                "residentialAddress" : "居住地址",
                "verified" : "是否实名认证",
                "type" : "技师类型",
                "source" : "注册渠道",
                "seniority" : "工龄",
                "createdUser" : "创建人",
                "createdTime" : "创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "description" : "描述"  
              }   
            }
        ],
        "totalCount":0
    }
}
```





