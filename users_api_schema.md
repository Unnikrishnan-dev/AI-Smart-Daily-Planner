# API schema for User

#### Create task
===========
```
API URL: Request:POST http://localhost:7072/api/users
```
Note: The domain will be changed once after the deployment of the API's

##### Request body
-----------
```
{
"user_name":"",
"user_email":"",
"role":""
}
```

##### Response 
--------
```
200 Ok with user created successfully
```
##### Error 
-----
```
500: internal server error <br>
400: bad request
```
#### Get Users:
=========
```
API URL::GET http://localhost:7072/api/users
```
Note: The domain will be changed once after the deployment of the API's
##### Response
---------
200 Ok
```
{
"user_name":"",
"user_email":""
"role":"",
"id:"id of the doc"
}
```
##### Error 
-----
```
500: internal server error <br>
400: bad request
```

#### Delete User:
===========
```
API URL::DELETE http://localhost:7072/api/users
```
Note: The domain will be changed once after the deployment of the API's
##### Request body:
-------------
```
{
  Ids:[<id>,<id>] // for multiple task deletion
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
500: internal server error,<br>
400: bad request
```