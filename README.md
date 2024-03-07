# urdoing
Urdoing Api Specifications and Guidlines
urdoing stands for "Uniform Resource + Doing",it aims an simple and powerfull style of api designing method.it's inspired both  by REST and rpc style api.

for example ， to design  users apis ,it will be this way in urdoing:

- Query one user info:            POST  /users/read     -d '[{"user_id":123456}]'
- Query two or more users info:   POST  /users/read     -d '[{"user_id":123456},{"user_id":891011},...]'
- Update one user info:           POST  /users/update   -d '[{"user_id":123456,user_info_to_update:{...}]'
- Update two or more users info:  POST  /users/update   -d '[{"user_id":123456,other_info...},{"user_id":7891011,other_info...}]'
- Create one user                 POST  /users/create   -d '[{"user_id":123456,user_info_to_create:{...}]'
- Create two or more  users:      POST  /users/create   -d '[{"user_id":123456,other_info...},{"user_id":7891011,other_info...}]'
- Delete one user                 POST  /users/delete   -d '[{"user_id":123456}]'
- Delete two or more users        POST  /users/delete   -d '[{"user_id":123456},{"user_id":891011},...]'
- 
Aditionally,for some special operations,wo can add custom action freely,for example ,we need to merge two users in to one,we could do it in this way:

- Merge two users into one        POST  /users/merge  -d '[{"user_id":123456},{"user_id":891011},...]'


In this way, we are able to implement all the functionality of REST and RPC-style APIs in a simpler, more powerful, and more consistent way。
