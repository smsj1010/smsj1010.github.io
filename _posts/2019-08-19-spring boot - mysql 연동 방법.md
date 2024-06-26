---
layout: single
title:  "spring boot - mysql 연동 방법"
categories: spring-cloud
tag: [spring-boot, jpa] 
toc: false
author_profile: false
sidebar:
    nav: "counts"
search: true
---

JPA + mysql 접속 방법 시, application.properties 파일 내용

## application.properties 설정
- mysql docker 실행 시 `-e "TZ=Asia/Seoul"` 인 경우, `serverTimezone=Asia/Seoul` 을 추가
- mysql table schema 가 대문자인 경우, 테이블 및 컬럼명을 못 찾는 문제 발생. 
  `org.hibernate.boot.model.naming.PhysicalNamingStrategyStandardImpl` 추가

```properties 
spring.jpa.hibernate.ddl-auto=none
# 테이블명 대문자 처리
spring.jpa.hibernate.naming.physical-strategy=org.hibernate.boot.model.naming.PhysicalNamingStrategyStandardImpl
# TimeZone 설정
spring.datasource.url=jdbc:mysql://${MYSQL_HOST:localhost}:3306/{데이터베이스명}?serverTimezone=Asia/Seoul 
spring.datasource.username={사용자명}
spring.datasource.password={비밀번호}
```

