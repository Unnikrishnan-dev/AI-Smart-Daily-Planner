
# API Schema for Task

#### Create Task:

```
API URL: Request:POST http://localhost:7072/api/task
```

Note: The domain will be changed once after the deployment of the API's

##### Request Body
------------
```
{
"description":"<description of the task>",
"task_type":"personal,work etc"
"reminder":"true/false"// this is basically determine the notfication on or off,
"reminder_time":"at what time notification should be send for the task"
"created_by":"logged in user who create",
"created_at":"time in utc"
}
```

##### Response 
--------
```
200 Ok with Task created successfully
```
##### Error 
-----
```
500: internal server error <br>
400: bad request
```

#### Get Task:
=========
```
API URL: Request:GET http://localhost:7072/api/task
```
Note: The domain will be changed once after the deployment of the API's
##### Response
---------
200 Ok
```
{
"description":"<description of the task>",
"task_type":"personal,work etc"
"reminder":"true/false",
"id:"id of the doc"
}
```

##### Error 
-----
```
500: internal server error <br>
400: bad request
```

#### Delete Task:
===========
```
API URL: Request:DELETE http://localhost:7072/api/task
```
Note: The domain will be changed once after the deployment of the API's
##### Request body:
-------------
```
{
  Ids:["id","id"] // for multiple task deletion
}
```

##### Response
--------
```
204 : content not found
```

##### Error 
-----
```
500: internal server error <br>
400: bad request
```
