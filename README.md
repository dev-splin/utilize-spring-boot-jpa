# :page_with_curl: 스프링 부트와 JPA 활용1

**[실전! 스프링 부트와 JPA 활용1 - 웹 애플리케이션 개발](https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8-JPA-%ED%99%9C%EC%9A%A9-1/dashboard)** 을 보며 제작한 Spring Boot + JPA 프로젝트입니다.





## :hammer: 설치

1. 프로젝트 생성 - **https://start.spring.io/**
   - Project : Gradle - Groovy
   - Language : Java
   - Spring Boot : 2.7.6
   - Group : jpabook
   - Artifact : jpashop
   - Packaging : Jar
   - Java : 17
   - Dependencies : `Thymeleaf`, `Spring Web`, `Spring Data JPA`, `H2 Database`, `Lombok`
2. h2(실습용 데이터베이스) 1.4.200버전 사용 - [링크 클릭](https://h2database.com/)
   - 데이터베이스 파일 생성 방법
     - `jdbc:h2:~/jpashop` (최소 한번)
     - `~/jpashop.mv.db` 파일 생성 확인
     - 이후 부터는 `jdbc:h2:tcp://localhost/~/jpashop` 이렇게 접속





## :eyes: View 환경 설정

View 환경은 Spring에서 밀어주는 thymeleaf를 사용합니다.

- 공식 사이트 : **[https://www.thymeleaf.org/](https://www.thymeleaf.org/)**
- 스프링 공식 튜토리얼 : **[https://spring.io/guides/gs/serving-web-content/](https://spring.io/guides/gs/serving-web-content/)**
- 스프링 부트 메뉴얼 : **[https://docs.spring.io/spring-boot/docs/2.1.6.RELEASE/reference/html/boot-features-developing-web-applications.html#boot-features-spring-mvc-template-engines](https://docs.spring.io/spring-boot/docs/2.1.6.RELEASE/reference/html/boot-features-developing-web-applications.html#boot-features-spring-mvc-template-engines)**



### 실시간 업데이트 하는 방법

Srping에서 View를 수정하면, 서버를 재시작해야합니다. 이 방법은 매우 불편하기 때문에 아래 방법을 통하여 실시간으로 업데이트를 확인할 수 있습니다.

1. dependencies에 `implementation 'org.springframework.boot:spring-boot-devtools'` 추가
   - 해당 방법을 사용하면 build 시 [restartedMain]이라고 나옵니다.
2. html 파일 수정 후 `Build -> Recompile(Ctrl + Shift + F9)`
3. 페이지 새로고침 후 업데이트된 사항 확인

위 방법이 적용되지 않는다면 아래 링크를 참고하시면 좋을 것 같습니다.

- 참고 링크 : **[https://lejewk.github.io/springboot-devtool/](https://lejewk.github.io/springboot-devtool/)**
