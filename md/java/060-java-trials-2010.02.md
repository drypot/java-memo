# 자바 삽질의 기록 2010.02

2010-11-28 14:18

Groovy 로 데모 코드 만들 때는 웹 라우터를 직접 간단히 만들어 썼었고,
출력은 Groovy Markup Builder 로 했으니, 아파치 업로더와 Groovy 외에 아무 것도 필요 없었는데,
다이나믹 언어에서 다시 나가려니 이런 것들 고민을 다시 해야하게 되었다.

프리젠테이션 레이어로 뭘 쓸까 Velocity, Sitemesh, JSP, Freemarker 들춰봤는데, 다들 좀 이상하다. =,=
오브젝트 타입 유지가 안 되거나, 사이트 템플릿을 만들어 쓰기가 힘들거나,
상심해서 일단 덮고.

MVC 류 웹 프레임웍들에서도 이상하게 타입 유지가 잘 안 되는 것 같다.
ASP.NET MVC 에서는 타입 유지가 되어서 뷰 페이지에서도 인델리센스가 잘 작동했었는데.

기본 웹 프레임웍으로 Java EE 5 문서나 Spring 2.X 문서들 보면,
잘 나가다가 XML 파일 한가득 나오면 질려서 또 덮어 버리고. =,=

지난 10 년간 우리나라 자바 개발자들 얼마나 고생했을까 싶다.

이거참, 뷰 프레임웍도 문제고, 로직 프레임웍도 문제니,
큰 맘먹고 10 년만에 자바로 왔는데 Ruby 나 Groovy 같은 다이나믹 언어 대신,
Java 나 Scala 같은 스터틱 언어로 자바 플랫폼에서 웹 개발을 할 수 있을까 회의감이 자꾸 든다.

웹 쪽에 답이 안 나와서 일단 Solaris, Maven 문서 한달 넘게 보면서 지내다가
며칠 전부터 작년 12 월에 막 나온 Java EE 6 문서를 읽기 시작했는데,
아, 이건 먼가 될 것 같다는 느낌이 온다.
(하지만 이것도 역시나였다. =,=)

Web Beans 버스가 일단 환상이 되었다.
오브젝트 라이프사이클 관리 알아서 해주니 일일이 신경쓸 필요가 없을 것 같고,
서로 연결하는데 어노테이션 덕분에 XML 도 필요 없고, 뷰하고도 막바로 연결 된다.
당연히 타입 안정성 확보하리라 예상을 해본다.

그리고 Facelet 이 표준으로 새로 들어갔던데 이것도 아주 좋다.
Sitemesh 같은 서드 파티 라이브러리 도움 없이 사이트 전체 템플릿도 만들 수 있게 되었다.
이런 당연한 기능이 이제 들어간 것에 감동해야하는 상황이 좀 이상하지만, 이제 되는 것 같다.
(JSP 로도 대충 되는데 이 땐 몰랐다.)

Web Beans + Facelets + JSF 2.0 요거 3 개만 가지고도 기존에 고민했던 문제들이 싹 사라져서,
새벽에 마음이 무척 밝아졌다.

Java EE 6 본 다음 문제 해결 안 되면 Spring 3 쪽도 검토하려고 했는데,
Spring 3 보고 고민거리만 더하지 말고 걍 Java EE 6 에 주저 앉아 버려도 될 것 같다.
걍 이정도면 충분할 것 같다.
GlassFish 만 깔면 더 이상 먼가 설치할 것이 필요 없다는 장점도 있고.

올해 예술기금신청에는 모두 낙방하였다. =,=