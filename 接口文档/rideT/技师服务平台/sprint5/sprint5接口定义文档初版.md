#### 1.1 查询岗位工种基础配置数据接口

接口名称：/postandworktype/getPostOrWorkTypeById

请求方式：POST

请求报文：

```java
{
   "post_id":"岗位ID",
   "work_type_id":"工种ID"
}
```

返回报文：

```java
{
    "code":0,
	"msg":"成功",
    "data":
    [
        {
        "code":"岗位编号",
        "name":"岗位名称",
        "description":"描述",
        "active":"是否启用：true/false",
        "work_types":[
               {
                "post_id":"所属岗位编号",
                "code":"工种编号",
                "name":"工种名称",
                "level_code":"等级编号",
                "level_name":"等级名称",
                "description":"描述",
                "active":"是否启用：true/false"
                }
            ]    
            
        }
    ]
}
```



#### 1.2职称信息列表全查询

接口名称：/tech-certification/professionaltitle/queryProfessionalTitleAllList

请求方式：POST

请求报文：

```java
{
                
}
```

返回报文：

```java
{
    "code":0,
    "msg":"成功"
        "data":[
            {   "name":"职称名称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "postName":"岗位名称",
                "workTypeName":"工种名称",
                "workTypeLevelName":"工种等级名称",
                "authorityType":"认证类型",
                "authority":"发证机构",
                "status":"职称状态",
                "activeTerm":"职称默认有效期",
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
            {   "name":"职称名称",
                "levelCode":"职称等级编号",
                "levelName":"职称等级名称",
                "postName":"岗位名称",
                "workTypeName":"工种名称",
                "workTypeLevelName":"工种等级名称",
                "authorityType":"认证类型",
                "authority":"发证机构",
                "status":"职称状态",
                "activeTerm":"职称默认有效期",
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
               
        ]
}
```

