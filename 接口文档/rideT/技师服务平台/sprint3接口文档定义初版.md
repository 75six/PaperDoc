# 1.培训服务

#### 1.1 查询面授培训列表数据接口 

接口名称：/training/getTrainingList 

请求方式：POST

请求报文：

```java
{
    "title" : "课程名称（模糊查询）",    
    "categoryId" : "分类ID"，   
    "courseType" :"课程类型"，     
    "status" : "发布状态" ，
    "teaching_status":"教学状态"  
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
        "id":1,                               
        "uid":"标志id", 
        "title":"课程名称",       
        "price":"价格",	
        "cover_img":"课程封面",	
        "category_id":"分类ID",
        "category_path":"分类路径",
        "credit" : "学分",
        "status":"发布状态",
        "teaching_status":"教学状态",                               
        "recommend":"是否推荐：true/false", 
        "audit_required":"报名是否需要审核：true/false",       
        "enrollment_required":"是否需要报名：true/false",	
        "exam_id":"课程考试id",	
        "enable_exam":"是否启用考试：true/false",
        "active_days":"有效天数",
        "created_user" : "创建时间",
        "updated_user":"更新时间",
        "created_time" : "创建时间",
        "updated_time":"更新时间",
        "description":"课程简介",
        "notice":"课程须知"，
        "objective":"课程目标"   

	},
        {
        "id":1,                               
        "uid":"标志id", 
        "title":"课程名称",       
        "price":"价格",	
        "cover_img":"课程封面",	
        "category_id":"分类ID",
        "category_path":"分类路径",
        "credit" : "学分",
        "status":"发布状态",
        "teaching_status":"教学状态",                               
        "recommend":"是否推荐：true/false", 
        "audit_required":"报名是否需要审核：true/false",       
        "enrollment_required":"是否需要报名：true/false",	
        "exam_id":"课程考试id",	
        "enable_exam":"是否启用考试：true/false",
        "active_days":"有效天数",
        "created_user" : "创建时间",
        "updated_user":"更新时间",
        "created_time" : "创建时间",
        "updated_time":"更新时间",
        "description":"课程简介",
        "notice":"课程须知"，
        "objective":"课程目标"   

	}
    ]
}
```

#### 1.2 新增面授培训课程接口 

接口名称：/training/addTraining 

请求方式：POST

请求报文：

```java
{    
        "title":"课程名称",       
        "price":"价格",	
        "cover_img":"课程封面",	
        "category_id":"分类ID",
        "category_path":"分类路径",
        "credit" : "学分",
        "status":"发布状态",
        "teaching_status":"教学状态",                               
        "recommend":"是否推荐：true/false", 
        "audit_required":"报名是否需要审核：true/false",       
        "enrollment_required":"是否需要报名：true/false",	
        "exam_id":"课程考试id",	
        "enable_exam":"是否启用考试：true/false",
        "active_days":"有效天数",
        "description":"课程简介",
        "notice":"课程须知"，
        "objective":"课程目标"   
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

#### 1.3 根据id查询面授培训课程信息 

接口名称：/training/getTrainingInfoById 

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
    "id":1,                               
    "uid":"标志id", 
    "title":"课程名称",       
    "price":"价格",	
    "cover_img":"课程封面",	
    "category_id":"分类ID",
    "category_path":"分类路径",
    "credit" : "学分",
    "status":"发布状态",
    "teaching_status":"教学状态",                               
    "recommend":"是否推荐：true/false", 
    "audit_required":"报名是否需要审核：true/false",       
    "enrollment_required":"是否需要报名：true/false",	
    "exam_id":"课程考试id",	
    "enable_exam":"是否启用考试：true/false",
    "active_days":"有效天数",
    "created_user" : "创建时间",
    "updated_user":"更新时间",
    "created_time" : "创建时间",
    "updated_time":"更新时间",
    "description":"课程简介",
    "notice":"课程须知",
    "objective":"课程目标"  
}
}
```

#### 1.4  根据id修改面授培训课程信息  

接口名称：/training/updateTrainingInfoById 

请求方式：POST

请求报文：

```java
{
    "id":1,                               
    "uid":"标志id", 
    "title":"课程名称",       
    "price":"价格",	
    "cover_img":"课程封面",	
    "category_id":"分类ID",
    "category_path":"分类路径",
    "credit" : "学分",
    "status":"发布状态",
    "teaching_status":"教学状态",                               
    "recommend":"是否推荐：true/false", 
    "audit_required":"报名是否需要审核：true/false",       
    "enrollment_required":"是否需要报名：true/false",	
    "exam_id":"课程考试id",	
    "enable_exam":"是否启用考试：true/false",
    "active_days":"有效天数",
    "created_user" : "创建时间",
    "updated_user":"更新时间",
    "created_time" : "创建时间",
    "updated_time":"更新时间",
    "description":"课程简介",
    "notice":"课程须知",
    "objective":"课程目标"  
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

#### 1.5  根据id修改面授培训课程状态

 接口名称：/training/updateTrainingStatusById 

请求方式：POST

请求报文：

```java
{
    "id":1, 
    "status":"发布状态"
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

# 2.分类服务

#### 2.1 删除岗位配置数据接口 

接口名称：/postandworktype/certificationauthority/deleteCertificationAuthority

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

#### 2.2 删除工种配置数据接口 

接口名称：/postandworktype/deleteWorkTypeById 

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

#### 2.3 修改岗位配置数据接口 

接口名称：/postandworktype/updatePostById 

请求方式：POST

请求报文：

```java
{
    "id":0,
    "code":"岗位编号",
    "name":"岗位名称",
    "description":"描述",
    "active":"是否启用：true/false"
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

#### 2.4 修改工种配置数据接口 

接口名称：/postandworktype/updateWorkTypeById 

请求方式：POST

请求报文：

```java
{
    "id":0,
    "post_id":"所属岗位编号",
    "code":"工种编号",
    "name":"工种名称",
    "level_code":"等级编号",
    "level_name":"等级名称",
    "description":"描述",
    "active":"是否启用：true/false"
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

#### 2.5 添加岗位配置接口 

接口名称：/postandworktype/addPost

请求方式：POST

请求报文：

```java
{
    "code":"岗位编号",
    "name":"岗位名称",
    "description":"描述",
    "active":"是否启用：true/false"
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

#### 2.4 添加工种配置数据接口 

接口名称：/postandworktype/addWorkTypeById 

请求方式：POST

请求报文：

```java
{
    "post_id":"所属岗位编号",
    "code":"工种编号",
    "name":"工种名称",
    "level_code":"等级编号",
    "level_name":"等级名称",
    "description":"描述",
    "active":"是否启用：true/false"
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

#### 2.5 查询岗位工种基础配置数据接口 

接口名称：/postandworktype/getPostAndWorkTypeInfo 

请求方式：POST

请求报文：

```java
{
   "post_id":"若为空则查全部"
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
                },
            {
                "post_id":"所属岗位编号",
                "code":"工种编号",
                "name":"工种名称",
                "level_code":"等级编号",
                "level_name":"等级名称",
                "description":"描述",
                "active":"是否启用：true/false"
                },
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

#### 