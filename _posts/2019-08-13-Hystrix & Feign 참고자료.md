---
layout: single
title:  "Hystrix & Feign 참고자료"
categories: spring-cloud
tag: [spring-boot, Hystrix, Feign] 
toc: false
author_profile: false
sidebar:
    nav: "counts"
search: true
---

- [Reference guide](https://cloud.spring.io/spring-cloud-static/spring-cloud-openfeign/2.2.0.M1/)

- [How-it-Works](https://github.com/Netflix/Hystrix/wiki/How-it-Works)

- [GETTING STARTED - Circuit Breaker](https://spring.io/guides/gs/circuit-breaker/)

- 개인 블로그

  [Springboot hystrix 사용기](https://jeong-pro.tistory.com/183)

  [Netflix Hystrix](https://multifrontgarden.tistory.com/238)

  [(Spring Cloud) Feign](https://supawer0728.github.io/2018/03/11/Spring-Cloud-Feign/)

  [우아한 Feign 적용기](http://woowabros.github.io/experience/2019/05/29/feign.html)


### 클라이언트 회복성 패턴

- 클라이언트 측 부하 분산
- 폴백 (fallback)
- 회로 차단기 (circuit breaks) - 빠른 실패 (fail fast), 원만한 실패 (fail gracefully), 원활한 회복 (recovery seamlessly)
- 벌크헤드 (bulkhead)

![Hystrix bulkhead](/images/Hystrix-bulkhead.png)
