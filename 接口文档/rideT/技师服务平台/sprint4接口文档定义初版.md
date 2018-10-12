# 1.技师管理		

#### 1.1注册技师

接口名称： /user/addUser 

请求方式：POST

描述：![1539339188078](C:\Users\ZHANGH~1\AppData\Local\Temp\1539339188078.png)

请求报文：

```java
{
       
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
    "seniority" : "工龄",
    "createdUser" : "创建人",
    "createdTime" : "创建时间",
    "updatedUser" : "更新人",
    "updatedTime" : "更新时间",
    "description" : "描述",
    "postInfo":
    {
       "shopId":"门店编号",
       "postCode":"岗位编号",
       "postName":"岗位名称",
       "techType":"技师类型"      
    },
    "workTypeInfo":
    {
       "shopId":"门店编号",
       "Code":"岗位编号",
       "name":"岗位名称",
       "levelCode":"岗位编号",
       "levelName":"岗位名称"       
    }
}
```

返回报文：

```java
{
	"code":0,
	"msg":"成功",
	"data":
    {
        "id":0,
        "accountId":0
    }
}
```





#### 1.2 新增职称信息

接口名称：/user/updateUserById

请求方式：POST

请求报文：

```java
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
    "seniority" : "工龄",
    "createdUser" : "创建人",
    "createdTime" : "创建时间",
    "updatedUser" : "更新人",
    "updatedTime" : "更新时间",
    "description" : "描述",
     "postInfo":
    {
       "shopId":"门店编号",
       "postCode":"岗位编号",
       "postName":"岗位名称",
       "techType":"技师类型"      
    },
    "workTypeInfo":
    {
       "shopId":"门店编号",
       "Code":"岗位编号",
       "name":"岗位名称",
       "levelCode":"岗位编号",
       "levelName":"岗位名称"       
    }
}
```

返回报文：

```java
{
    "code":0,
	"msg":"成功",
    "data":{
        "result":true
    }
}
```

#### 1.3根据技师id查询技师信息

接口名称：/user/getUserInfoById

请求方式：POST

备注：查询数据时，需过滤所有未启用/已删除的信息

[^personnelInfo]: 用户人事信息<  表名：user_personnel_info >
[^companyInfo]: 用户所属公司< 表名：user_company >
[^postList]: 用户岗位信息< 表名： user_post >
[^workTypeList]: 用户工种信息< 表名： user_work_type >
[^professionalTitleInfo]: 用户职称信息< 表名：user_professional_title>

请求报文：

```java
{
    "id"  : 0
}
```

返回报文：

```java
{
    "code":0,
	"msg":"成功",
    "data":{
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
    "seniority" : "工龄",
    "createdUser" : "创建人",
    "createdTime" : "创建时间",
    "updatedUser" : "更新人",
    "updatedTime" : "更新时间",
    "description" : "描述",
    "personnelInfo" : 
        {
        "id":"用户人事信息id",
        "status":"人事状态",
        "staffingType":"人员编制",
        "wage":"工资",
        "entryTime":"入职时间",
        "leaveTime":"离职时间",
        "trainingStatus":"培训状态",
        "contactTime":"合同时间",
        "monthlyAllowance":"每月补贴",
        },  
     "companyInfo":
        {
        "id":"所属公司id",
        "code":"公司编号",
        "name":"公司名称",
        "abbreviation":"公司简称",
        "createdUser":"创建用户",
        "createdTime":"创建时间",
        "updatedUser" : "更新人",
        "updatedTime" : "更新时间",
        "description" : "描述"    
        },
      "postList":
        [
            {
                "id":"用户岗位id",
                "shopId":"门店编号",
                "postCode":"岗位编号",
                "postName":"岗位名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "techType":"技师类型"
            },
            {
                "id":"用户岗位id",
                "shopId":"门店编号",
                "postCode":"岗位编号",
                "postName":"岗位名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "techType":"技师类型"
            },
        ],
     "workTypeList":
        [
            {
                "id":"用户工种id",
                "code":"岗位编号",
                "name":"岗位名称",
                "levelCode":"等级编号",
                "levelName":"等级名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间"
            },
            {
                "id":"用户工种id",
                "code":"岗位编号",
                "name":"岗位名称",
                "levelCode":"等级编号",
                "levelName":"等级名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间"
            },
        ],
     "professionalTitleInfo":
        [
            {
                "id":"用户职称id",
                "titleId":"职称id",
                "name":"职称名称",
                "simpleName":"证书简称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "certificateId":"证书识别码",
                "postCode":"岗位编号",
                "workTypeCode":"工种编号",
                "certificationType":"认证类型",
                "authorityId":"发证机构id",
                "authorityName":"发证机构名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "status":"职称等级",
                "activeTerm":"职称默认有效期",
                "description":"描述"
            },
            {
                "id":"用户职称id",
                "titleId":"职称id",
                "name":"职称名称",
                "simpleName":"证书简称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "certificateId":"证书识别码",
                "postCode":"岗位编号",
                "workTypeCode":"工种编号",
                "certificationType":"认证类型",
                "authorityId":"发证机构id",
                "authorityName":"发证机构名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "status":"职称等级",
                "activeTerm":"职称默认有效期",
                "description":"描述"
            }
        ]
    }
}
```

#### 1.3根据技师id查询技师信息

接口名称：/user/getUserInfoByAccountId

请求方式：POST

备注：查询数据时，需过滤所有未启用/已删除的信息

[^personnelInfo]: 用户人事信息<  表名：user_personnel_info >
[^companyInfo]: 用户所属公司< 表名：user_company >
[^postList]: 用户岗位信息< 表名： user_post >
[^workTypeList]: 用户工种信息< 表名： user_work_type >
[^professionalTitleInfo]: 用户职称信息< 表名：user_professional_title>

请求报文：

```java
{
    "accountid"  : 0
}
```

返回报文：

```java
{
    "code":0,
	"msg":"成功",
    "data":{
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
    "seniority" : "工龄",
    "createdUser" : "创建人",
    "createdTime" : "创建时间",
    "updatedUser" : "更新人",
    "updatedTime" : "更新时间",
    "description" : "描述",
    "personnelInfo" : 
        {
        "id":"用户人事信息id",
        "status":"人事状态",
        "staffingType":"人员编制",
        "wage":"工资",
        "entryTime":"入职时间",
        "leaveTime":"离职时间",
        "trainingStatus":"培训状态",
        "contactTime":"合同时间",
        "monthlyAllowance":"每月补贴",
        },  
        "companyInfo":
        {
        "id":"所属公司id",
        "code":"公司编号",
        "name":"公司名称",
        "abbreviation":"公司简称",
        "createdUser":"创建用户",
        "createdTime":"创建时间",
        "updatedUser" : "更新人",
        "updatedTime" : "更新时间",
        "description" : "描述"    
        },
        "postList":
        [
            {
                "id":"用户岗位id",
                "shopId":"门店编号",
                "postCode":"岗位编号",
                "postName":"岗位名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "techType":"技师类型"
            },
            {
                "id":"用户岗位id",
                "shopId":"门店编号",
                "postCode":"岗位编号",
                "postName":"岗位名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "techType":"技师类型"
            },
        ],
        "workTypeList":
        [
            {
                "id":"用户工种id",
                "code":"岗位编号",
                "name":"岗位名称",
                "levelCode":"等级编号",
                "levelName":"等级名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间"
            },
            {
                "id":"用户工种id",
                "code":"岗位编号",
                "name":"岗位名称",
                "levelCode":"等级编号",
                "levelName":"等级名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间"
            },
        ]
     "professionalTitleInfo":
        [
            {
                "id":"用户职称id",
                "titleId":"职称id",
                "name":"职称名称",
                "simpleName":"证书简称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "certificateId":"证书识别码",
                "postCode":"岗位编号",
                "workTypeCode":"工种编号",
                "certificationType":"认证类型",
                "authorityId":"发证机构id",
                "authorityName":"发证机构名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "status":"职称等级",
                "activeTerm":"职称默认有效期",
                "description":"描述"
            },
            {
                "id":"用户职称id",
                "titleId":"职称id",
                "name":"职称名称",
                "simpleName":"证书简称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "certificateId":"证书识别码",
                "postCode":"岗位编号",
                "workTypeCode":"工种编号",
                "certificationType":"认证类型",
                "authorityId":"发证机构id",
                "authorityName":"发证机构名称",
                "createdUser":"创建用户",
                "createdTime":"创建时间",
                "updatedUser" : "更新人",
                "updatedTime" : "更新时间",
                "status":"职称等级",
                "activeTerm":"职称默认有效期",
                "description":"描述"
            }
        ]    
    }
}
```

#### 