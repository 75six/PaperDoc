# 1.字典表数据		

#### 1.1根据子类信息查询查询父类信息

接口名称： /shop-common/dictionary/getDictionaryParentByChild 

请求方式：POST

请求报文：

```java
{
    "id" : 0,    //字典ID，非必填
    "display_name" : "显示名称"   //显示名称，非必填
    "description" :"描述"     //相关描述，非必填
    "level" : 1 //向上查询层级，非必填，默认为1，即查询一层父级
}
```

返回报文：

```java
{
	"code":0,
	"msg":"成功",
	"data":
	{
     "id":1,                               
	"type":"表名-字段名", //类型
	"code":0,       //编号
	"diplay_name":"名称",	//显示值
	"description":"描述",	//描述
     "created_user":"创建人",
     "created_time":"创建时间",
     "updated_user" : "更新人",
     "updated_time":"更新时间",
	 "children":{
                "id":2,                               
                "type":"表名-字段名", //类型
                "code":0,       //编号
                "diplay_name":"名称",	//显示值
                "description":"描述",	//描述
                 "created_user":"创建人",
                 "created_time":"创建时间",
                 "updated_user" : "更新人",
                 "updated_time":"更新时间"
	}
	}
}
```



# 2.认证管理

#### 2.1 新增职称信息

接口名称：/tech-certification/professionaltitle/addProfessionalTitle

请求方式：POST

请求报文：

```java
{
    "name":"职称名称",
    "levelCode":"职称等级编号",
    "levelName":"职称等级名称",
    "postId":"岗位ID",
    "workTypeId":"工种ID",
    "authorityId":"发证机构ID",
    "status":"职称状态",
    "activeTerm":"职称默认有效期",
    "ruleList":[
        {
            "type":"条件类型",
            "value":"条件值"
        },
        {
            "type":"条件类型",
            "value":"条件值"
        },
        {
            "type":"条件类型",
            "value":"条件值"
        }
    ]
}
```

返回报文：

```java
{
    "code":0,
	"msg":"成功",
    "data":{
        "id":0
    }
}
```

#### 2.2更新职称信息

接口名称：/tech-certification/professionaltitle/updateProfessionalTitle

请求方式：POST

请求报文：

```java
{
    "id"  : 0,
    "name":"职称名称",
    "levelCode":"职称等级编号",
    "levelName":"职称等级名称",
    "postId":"岗位ID",
    "workTypeId":"工种ID",
    "authorityId":"发证机构ID",
    "status":"职称状态",
    "activeTerm":"职称默认有效期",
    "ruleList":[
        {
            "type":"条件类型",
            "value":"条件值"
        },
        {
            "type":"条件类型",
            "value":"条件值"
        },
        {
            "type":"条件类型",
            "value":"条件值"
        }
    ]
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

#### 2.3删除职称信息

接口名称：/tech-certification/professionaltitle/deleteProfessionalTitle

请求方式：POST

请求报文：

```java
{
    "id":0
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

#### 2.4查询职称信息

接口名称：/tech-certification/professionaltitle/getProfessionalTitleById

请求方式：GET

请求报文：

```
{
    id:0
}
```

返回报文：

```java
{
    "code":0,
    "msg":"成功"
        "data":
            { "name":"职称名称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "postId":"岗位ID",
                "workTypeId":"工种ID",
                "authorityId":"发证机构ID",
                "status":"职称状态",
                "activeTerm":"职称默认有效期",
                "createdBy":"创建人",
                "createdTime":"创建时间",
                "updatedBy":"更新人",
                "updatedTime":"更新时间",
                "isDeleted":true,
                "ruleList":[
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            },
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            },
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            }
                ]}
                
}
```

#### 2.5根据条件查询职称信息列表页

接口名称：/tech-certification/professionaltitle/serachProfessionalTitleList

请求方式：POST

请求报文：

```java
{
                "name":"职称名称（模糊查询）",
                "levelCode":"职称等级编号",
                "postId":"岗位ID",
                "workTypeId":"工种ID",
                "authorityType":"认证类型",
                "authorityId":"发证机构ID",
                "pageNo": 0,
                "pageSize": 0,
                "sortBy": "string"
}
```

返回报文：

```java
{
    "code":0,
    "msg":"成功"
        "data":{
            "titleList":[
            { "name":"职称名称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "postId":"岗位ID",
                "workTypeId":"工种ID",
                "authorityType":"认证类型",
                "authority":"发证机构",
                "status":"职称状态",
                "activeTerm":"职称默认有效期",
                "createdBy":"创建人",
                "createdTime":"创建时间",
                "updatedBy":"更新人",
                "updatedTime":"更新时间",
                "ruleList":[
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            },
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            },
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            }
                ]},
            { "name":"职称名称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "postId":"岗位ID",
                "workTypeId":"工种ID",
                "authorityType":"认证类型",
                "authority":"发证机构",
                "status":"职称状态",
                "activeTerm":"职称默认有效期",
                "createdBy":"创建人",
                "createdTime":"创建时间",
                "updatedBy":"更新人",
                "updatedTime":"更新时间",
                "ruleList":[
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            },
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            },
                            {
                                "type":"条件类型",
                                "value":"条件值",
                                "isActive":"是否启用"
                            }
                ]}
               
        ],
            "totalCount":0
        }
}
```



# 3.发证机构表维护

#### 3.1 新增发证机构信息

接口名称：/tech-certification/certificationauthority/addCertificationAuthority

请求方式：POST

请求报文：

```java
{
    "name":"认证机构名称",
    "brand":"机构所属品牌",
    "description":"描述"
}
```

返回报文：

```java
{
    "id":0
}
```

#### 3.2 更新发证机构信息

接口名称：/tech-certification/certificationauthority/updateCertificationAuthority

请求方式：POST

请求报文：

```java
{
    "id":0,
    "name":"认证机构名称",
    "brand":"机构所属品牌",
    "description":"描述",
    "isActive":true
}
```

返回报文：

```java
{
    "code":0,
    "msg":"成功",
    "data":true
}
```

#### 3.3 删除发证机构信息

接口名称：/tech-certification/certificationauthority/deleteCertificationAuthority

请求方式：POST

请求报文：

```java
{
    "id":0
}
```

返回报文：

```java
{
    "code":0,
    "msg":"成功",
    "data":true
}
```

#### 3.3 根据ID查询发证机构信息

接口名称：/tech-certification/certificationauthority/getCertificationAuthorityById

请求方式：GET

请求报文：

```java
{
    "id":0
}
```

返回报文：

```java
{
    "code":0,
    "msg":"成功",
    "data":{
        "id":0,
        "name":"认证机构名称",
        "brand":"机构所属品牌",
        "description":"描述",
        "isActive":true,
        "createdBy":"创建人",
        "createdTime":"创建时间",
        "updatedBy":"更新人",
        "updatedTime":"更新时间"
    }
}

```

#### 3.3 查询发证机构信息列表

接口名称：/tech-certification/certificationauthority/getCertificationAuthorityList

请求方式：GET

请求报文：(空)

返回报文：

```java
{
    "code":0,
    "msg":"成功",
    "data":[{
        "id":0,
        "name":"认证机构名称",
        "brand":"机构所属品牌",
        "description":"描述",
        "isActive":true,
        "createdBy":"创建人",
        "createdTime":"创建时间",
        "updatedBy":"更新人",
        "updatedTime":"更新时间"
         },
            {
        "id":0,
        "name":"认证机构名称",
        "brand":"机构所属品牌",
        "description":"描述",
        "isActive":true,
        "createdBy":"创建人",
        "createdTime":"创建时间",
        "updatedBy":"更新人",
        "updatedTime":"更新时间"
         },
           {
        "id":0,
        "name":"认证机构名称",
        "brand":"机构所属品牌",
        "description":"描述",
        "isActive":true,
        "createdBy":"创建人",
        "createdTime":"创建时间",
        "updatedBy":"更新人",
        "updatedTime":"更新时间"
         } 
           
           ]
}

```

