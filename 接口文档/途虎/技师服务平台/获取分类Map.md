获取分类Map

需求描述：根据业务要求，由课程列表页显示提出需要，传入分类id集合，提供相应的名称，以Key-Value的形式存入map返回

访问方式：GET
接口名称：/tech-data-setting/getCategoryMap

请求报文

```java
{
    ["id1","id2","id3"]  //请求的id集合
}
```

返回报文

```java
{
	"code":0,
	"msg":"成功",
	"data":{
    "id1":"name1",                               //分类id:分类名称
	"id2":"name2",                               //分类id:分类名称
     "id3":"name3"                              //分类id:分类名称
}
}
```

