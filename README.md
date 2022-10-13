# Today I Learn 학습한 내용들 정리! 

## Spring
### JPA

### Spring boot

### RestTemplate
    
    • Spring 3부터 지원, REST API 호출이후 응답을 받을 때까지 기다리는 동기 방식
    
### WebClient
    - Spring 5에 추가된 논블럭, 리엑티브 웹 클라이언트로 동기, 비동기 방식을 지원한다.

### Security

<br/>

## Web
### [JWT](https://github.com/yeonjiyeon/TIL/blob/main/web/JWT.md)

<br/>

## Java
### [JaCoCo](https://github.com/yeonjiyeon/TIL/blob/main/Java/JaCoCo.md)
### 디자인 패턴
#### Builder 패턴
#### observer 패턴

<br/>


## DataBase

## Redis 

## Docker

## Git

## 웹 공격 기술
### [XSS(크로스 사이트 스크립팅, cross-site scripting)](https://github.com/yeonjiyeon/TIL/blob/main/%EC%9B%B9%EA%B3%B5%EA%B2%A9%EA%B8%B0%EC%88%A0/XSS.md)

## Tool
### Postman
### IntelliJ
#### HttpClient
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
