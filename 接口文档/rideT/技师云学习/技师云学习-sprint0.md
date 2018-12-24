### 1、章节页面逻辑修改

#### 1.1新增学习记录

/study/addCourseUserLearning

请求方式：

```java
{
   
"userId":0,
"lessonId":0,
"isPass":true,
"duration":"视频长度",
"progress":"观看进度",
"studyDuration":"视频学习长度",
"description":"描述"

}
```

返回报文：

```java
{
    "code":0,
	"msg":"Success",
    "data":true
}
```

#### 1.2更新学习记录

/study/updateCourseUserLearning

请求方式：

```java
{
   
"userId":0,
"lessonId":0,
"isPass":true,
"duration":"视频长度",
"progress":"观看进度",
"studyDuration":"视频学习长度",
"description":"描述"

}
```

返回报文：

```java
{
    "code":0,
	"msg":"Success",
    "data":true
}
```

#### 

### 2、实操视频上传接口

#### 2.1 实操视频上传接口

##### /study/uploadPraticalOperation

请求方式：POST

请求报文：

```java
{
    "userId":0,
    "lessonId":0,
    "videoUrl":"视频地址",
    "frame":"视频第一帧截图"
}
```

返回报文：

```java
{
    "code":0,
	"msg":"Success",
    "data":true
}
```



#### 2.2 实操认证查询详情

##### /study/getPraticalOperationInfo

请求方式：POST

请求报文：

```java
{
    "userId":0,
    "lessonId":0
}
```

返回报文：  

```java
{
    "code":0,
	"msg":"Success",
    "data":{
              "id":0,
              "userId":"用户编号",
              "lessonId":"所属课程编号",
              "auditStatus":"审核状态",
              "auditTime":"审核时间",
              "freezeTime":"冻结时间"
    }
}
```

#### 

#### 2.3 实操认证列表查询接口

##### /study/getPraticalOperationList

请求方式：POST

请求报文：

```java
{
    
    "userName":"用户名称",
    "lessonId":0,
    "auditStatus":"审核状态",
    "auditTime":"审核时间",
    "startSubmitTime":"开始提交时间",
    "endSubmitTime":"结束提交时间",
    "createdUser":"创建人",
    "pageNo": 0,
    "pageSize": 0,
    "sortBy": "string"    
}
```

返回报文：  

```java
{
    "code":0,
	"msg":"Success",
    "data":{
        "list":[
            {
              "id":0,
              "userName":"用户名称",
              "lessonName":"所属课程名称",
              "phoneNo":"用户手机号（mark）",
              "auditStatus":"审核状态",
              "auditTime":"审核时间",
              "startSubmitTime":"开始提交时间",
              "endSubmitTime":"结束提交时间",
              "createdTime":"提交时间"
            },
            {
              "id":0,
              "userName":"用户名称",
              "lessonName":"所属课程名称",
              "phoneNo":"用户手机号（mark）",
              "auditStatus":"审核状态",
              "auditTime":"审核时间",
              "startSubmitTime":"开始提交时间",
              "endSubmitTime":"结束提交时间",
              "createdTime":"提交时间"
           
            }
        ] ,
            "totalCount":0
    
    }
}
```

#### 2.4 实操认证接口

##### /study/authPraticalOperation

请求方式：POST

请求报文：

```java
{
    "id":0,
    "auditStatus":"1:通过,2：不通过", 
    "description"："备注"    
}
```

返回报文：

```java
{
    "code":0,
	"msg":"Success",
    "data":true
}
```

# 2.用户认证管理

#### 2.1 新增用户职称信息

接口名称：/study/addUserProfessionalTitle

请求方式：POST

请求报文：

```java
{
    "ti"
    "name":"职称名称",
    "levelCode":"职称等级编号",
    "levelName":"职称等级名称",
    "postId":"岗位ID",
    "workTypeId":"工种ID",
    "authorityId":"发证机构ID",
    "status":"职称状态",
    "activeTerm":"职称默认有效期",
    "theoryScore":"理论知识考试成绩"
    
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

#### 2.2查询用户职称信息

接口名称：/study/getUserProfessionalTitleById

请求方式：POST

请求报文：

```java
{
   "userId":0,
    "trainPlanId":0
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

#### 