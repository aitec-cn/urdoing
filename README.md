# urdoing
### Urdoing API Specifications and Guidlines

"urdoing" stands for "Uniform Resource Doing" ,it aims an simple and powerfull style of API designing method.It's inspired both  by REST and RPC style API.

For example ， to design users APIs ,each resource should provide some public doing(method) corresponding to curd operations：

Query noe user info:
```javascript
POST  /users/read     [{"user_id":123456}]
```
Query two or more users info:
```javascript
POST  /users/read     [{"user_id":123456},{"user_id":891011},...]
```
Update one user info:
```javascript
POST  /users/update   [{"user_id":123456,"user_info_to_update":"some_value",...]
```
Update two or more users info:
```javascript
POST  /users/update    [{"user_id":123456,"user_info_to_update":"some_value",...},{"user_id":891011,"user_info_to_update":"some_value",...}]
```
Create one user:
```javascript
POST  /users/create    [{"user_id":123456,"user_info_to_create":"some_value",...]
```
Create two or more  users:
```javascript
POST  /users/create    [{"user_id":123456,"user_info_to_create":"some_value",...},{"user_id":7891011,"user_info_to_create":"some_value",...}]
```
Delete one user:
```javascript
POST  /users/delete    [{"user_id":123456}]
```
Delete two or more users:
```javascript
POST  /users/delete    [{"user_id":123456},{"user_id":891011},...]
```
 
Aditionally,for some special operations,wo can add custom doing freely,for example ,we need to merge two users in to one,we could do it in this way:

Merge two users into one:
```javascript
POST  /users/merge  [{"user_id":123456},{"user_id":891011}]
```

In this way, we are able to implement all the functionality of REST and RPC-style APIs in a simpler, more powerful, and more consistent way.
