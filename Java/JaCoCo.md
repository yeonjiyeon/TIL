
- Jacoco : Java 코드의 커버리지를 체크하는 라이브러리

[https://techblog.woowahan.com/2661/](https://techblog.woowahan.com/2661/)

```groovy
//Gradle 설정에 JaCoCo 플러그인을 추가
plugins {
  id 'jacoco'
}

acocoTestReport {
    dependsOn tasks.test
    reports {
// 원하는 리포트를 켜고 끌 수 있습니다.
        xml.enabled(true)
        html.enabled(true)
//  각 리포트 타입 마다 리포트 저장 경로를 설정할 수 있습니다.
        xml.destination(new File("build/reports/jacoco.xml"))
    }
}

test {
  useJUnitPlatform()
}

//JUnit5로 테스트를 작생했기 때문에 테스트 시 JUnit이 함께 동작할 수 있도록 다음 설정을 해줍니다.
test {
  useJUnitPlatform()
}
```

- sonarqube버그, 코드 스멜, 보안 취약점을 발견할 목적으로 정적 코드 분석으로 자동 리뷰를 수행하기 위한 지속적인 코드 품질 검사용 오픈 소스 플랫폼

* 참고
https://techblog.woowahan.com/2661/