```java
###
POST http://localhost:8080/login
Content-Type:application/json

{
  "password": "1234567890",
  "userId": "user"
}

> {%client.global.set("auth_token",response.body.result.accessToken); %}

###
GET https://localhost:8080/user
Authorization: Bearer {{auth_token}}

###
GET http://localhost:8080/logout
Authorization: Bearer {{auth_token}}

<>2022-10-12T165849.401.json
<>2022-10-12T165827.200.json
```

Postman 대안으로 사용  가능

#### setting -> keymap : 단축키 찾기