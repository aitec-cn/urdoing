# urdoing
### Urdoing API Specifications and Guidlines

"urdoing" stands for "Uniform Resource + Doing",it aims an simple and powerfull style of API designing method.it's inspired both  by REST and rpc style API.

for example ， to design  users APIs ,it will be this way in urdoing:

Query noe user info:
```rust
POST  /users/read     -d '[{"user_id":123456}]'
```
Query two or more users info:
```rust
POST  /users/read     -d '[{"user_id":123456},{"user_id":891011},...]'
```
Update one user info:
```rust
POST  /users/update   -d '[{"user_id":123456,user_info_to_update:{...}]'
```
Update two or more users info:
```rust
POST  /users/update   -d '[{"user_id":123456,other_info...},{"user_id":7891011,other_info...}]'
```
Create one user:
```rust
POST  /users/create   -d '[{"user_id":123456,user_info_to_create:{...}]'
```
Create two or more  users:
```rust
POST  /users/create   -d '[{"user_id":123456,other_info...},{"user_id":7891011,other_info...}]'
```
Delete one user:
```rust
POST  /users/delete   -d '[{"user_id":123456}]'
```
Delete two or more users:
```rust
POST  /users/delete   -d '[{"user_id":123456},{"user_id":891011},...]'
```
 
Aditionally,for some special operations,wo can add custom action freely,for example ,we need to merge two users in to one,we could do it in this way:

Merge two users into one:
```rust
POST  /users/merge  -d '[{"user_id":123456},{"user_id":891011},...]'
```

In this way, we are able to implement all the functionality of REST and RPC-style APIs in a simpler, more powerful, and more consistent way.
