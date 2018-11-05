### 培训计划管理接口API

#####  1.1 查询培训计划管理列表接口

###### 功能描述：通过条件查询培训管理列表

##### 接口地址：/trainingPlan/getTrainingPlanList

##### 请求方式：POST

##### 请求参数格式：

~~~json
{
    "postData": {
        "name": "培训计划名称", 
        "professionalId": "职称证书", 
        "status": "状态",
        "pageSize":0,
        "totalCount":10
    }
}
~~~

##### 响应参数格式：

~~~json

{
    "code": 10000, 
    "message": "操作成功", 
    "data": {
        "totalCount": "总数据量", 
        "planList": [
            {
                "id": "id用于编辑",
                "name": "培训计划名称",
                "titleId":"目标职称",
                "studyPeriodType":"学习有效期类型",
                "studyDealine": "学习截止时间",
                "studyDays": "可学习天数",
                "createdUser":"创建人",
                "createdTime":"创建时间",
                "updatedUser": "更新人",
                "updatedTime": "更新时间",
                "status":"培训计划状态",
                "description": "描述"
                
            }]
    }
}
~~~

| 参数名          | 类型   | 是否必须 | 说明                                                   |
| --------------- | ------ | -------- | ------------------------------------------------------ |
| name            | String | N        | 培训计划名称,20字以内                                  |
| professionalId  | int    | N        | 职称证书 默认-1：全部证书                              |
| status          | int    | N        | 状态: 0：未发布 1：已发布 2：已关闭                    |
| studyPeriodType | int    | N        | 学习有效期类型:0：按有效天数 1：按截止日期 2：永久有效 |
| studyDealine    | Data   | N        | 学习截止时间                                           |
| studyDays       | int    | N        | 可学习天数                                             |
| description     | String | N        | 描述，字数200字以内                                    |



##### 1.2 查询培训计划详情接口

###### 功能描述：用于编辑时查询对应培训计划详情

##### 请求地址：/trainingPlan/getTrainingPlanById

##### 请求方式：GET

##### 请求参数格式：

~~~json
{
    id:"id"
}
~~~

##### 响应参数格式：

~~~json
{
    id: "id",
    name: "培训计划名称",
    titleId: "目标职称",
    studyPeriodType: "学习有效期类型",
    studyDeadline: "截至时间",
    studyDays: "学习天数",
    description: "培训计划简介",
    sectionName: "阶段名称",
    sectionType: "阶段类型",
    courseActive: "在线课程开关",
    trainActive: "面授课程开关",
    status: "发布状态",
    "sectionData":{
            "courseList":[{
                "name": "阶段名称",
                "type": "0",
                "description": "教学任务简介"
            }],
            "traningList" : [{
                "name" : "阶段名称",
                "type" : "1",
                "description" : "教学任务简介"
            }],
            "examList" : [{
                "name" : "阶段名称",
                "type" : "2"
            }]
    	}
}
~~~

| 参数名          | 类型   | 是否必须 | 说明                                                         |
| --------------- | ------ | -------- | ------------------------------------------------------------ |
| id              | int    | Y        | 培训计划ID                                                   |
| studyPeriodType | int    | N        | 学习有效期类型:0：按有效天数 1：按截止日期 2：永久有效       |
| studyDays       | int    | N        | 0天，表示永久有效,其他为对应天数                             |
| description     | String | N        | 用于介绍该培训计划，字数200字以内                            |
| sectionName     | String | N        | 阶段名称                                                     |
| sectionType     | int    | N        | 阶段类型：0：在线课程学习阶段 1：面授课程学习阶段 2:职业资格认证考试 |



##### 1.3 新增培训计划接口

###### 功能描述：新增培训计划

##### 请求地址：/trainingPlan/addTrainDetail

##### 请求方式：POST

##### 请求参数格式：

~~~json
{
    "postData": {
        "name": "培训计划名称", 
        "titleId": "目标职称", 
        "status": "培训计划状态",
        "studyPeriodType": "学习有效期类型",
        "studyDeadline": "截至时间",
        "studyDays": "可学习天数",
        "description": "培训计划简介",
        "courseActive": "在线课程开关",
        "trainActive": "面授课程开关",
        "sectionData":{
            "courseList":[{
                "name": "阶段名称",
                "type": "0",
                "description": "教学任务简介"
            }],
            "trainingList" : [{
                "name" : "阶段名称",
                "type" : "1",
                "description" : "教学任务简介"
            }],
            "examList" : [{
                "name" : "阶段名称",
                "type" : "2"
            }]
    	}
    }
}
~~~

##### 响应参数格式：

~~~json

{
    "code": 10000, 
    "message": "操作成功"
}
~~~

| 参数名          | 类型 | 是否必须 | 说明                                                   |
| --------------- | ---- | -------- | ------------------------------------------------------ |
| id              | int  | N        | id用于编辑时必传，新增可不传                           |
| status          | int  | Y        | 状态: 0：保存 1：发布 2：取消发布                      |
| studyPeriodType | int  | Y        | 学习有效期类型:0：按有效天数 1：按截止日期 2：永久有效 |



##### 1.4 编辑培训计划接口

###### 功能描述：编辑培训计划

##### 请求地址：/trainingPlan/	editTrainDetail

##### 请求方式：POST

##### 请求参数格式：

~~~json
{
    "id": "id",
    "postData": {
        "name": "培训计划名称", 
        "titleId": "目标职称", 
        "status": "培训计划状态",
        "studyPeriodType": "学习有效期类型",
        "studyDeadline": "截至时间",
        "studyDays": "可学习天数",
        "description": "培训计划简介",
        "courseActive": "在线课程开关",
        "trainActive": "面授课程开关",
        "sectionData":{
            "courseList":[{
                "name": "阶段名称",
                "type": "0",
                "description": "教学任务简介",
                "isDeleted" : "是否删除",
                "actionType": "add or edit"
            }],
            "trainingList" : [{
                "name" : "阶段名称",
                "type" : "1",
                "description" : "教学任务简介",
                "isDeleted" : "是否删除",
                "actionType" : "add or edit"
            }],
            "examList" : [{
                "name" : "阶段名称",
                "type" : "2",
                "isDeleted" : "是否删除",
                "actionType" : "add or edit"
            }]
    	}
    }
    
}

~~~

##### 响应参数格式：

~~~json

{
    "code": 10000, 
    "message": "操作成功"
}
~~~











