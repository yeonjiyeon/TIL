- ****WebSecurityConfigurerAdapter****

:스프링 시큐리티의 핵심적인 클래스, 스프링 시큐리티의 웹 보안 기능 초기화 및 설정등을 모두 처리하는 클래스이다! 

HttpSecurity 클래스를 생성한다.

- **HttpSecurity**

: 세부적인 보안 기능을 설정할 수 있는 API 제공한다.

강의 : 스프링 시큐리티(인프런) 

http.formLogin(): 폼 로그인 인증 기능 제공


**.loginPage(“/login.html") :** 로그인 페이지를 만들어 등록할 수 있음 

**.usernameParameter("username")	:** 유저네임을 유저네임 파라미터명이 아니라 다른 파라미터명으로 지정해 줄 수 있다.

**.passwordParameter(“password”) :** 패스워드를 ****패스워드 파라미터명이 아니라 다른 파라미터명으로 지정해 줄 수 있다. ****
