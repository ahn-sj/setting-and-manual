# JSP 이클립스 개발 환경
## JavaEE(Eclipse IDE for Java EE Developers)를 사용
<br>

### 이클립스에서 JSP 개발 시 아래의 과정들을 한 번에 처리
- 코드수정<br>
- 컴파일<br>
- 배포<br>
- 톰캣 서버 재시작<br>
- 브라우저로 요청<br><br>


## 프로젝트 생성
File -> new -> Dynamic Web project<br><br>

## 실행환경 설정
Target runtime<br>
new Runtime -> Select Apache Tomcat version -> Select installtion directory -> Finish<br><br>

## context명 변경
localhost:8080/JSPPrj/index.html<br>
이 있을 때 JSPPrj를 숨기는 것이 바람직함<br><br>

프로젝트 우클릭 -> Properties -> Web Preoject Settings -> Context root : JSPPrj를 /로 변경<br>
Tomcat Server Stop -> Remove context site -> Tomcat Server Restart<br><br>

 URL이 localhost:8080/index.html로 뜨면 정상적으로 변경됨<br><br>

 ## .java 경로
 프로젝트명 -> src/main/java<br><br>

 ## web.xml
 web.xml파일을 Tomcat폴더에서 복사해서<br>
 프로젝트명 - src/main/webapp/WEB-INF/web.xml이 위치하도록 붙여넣기<br><br>

## 문서 생성시 문자형식 설정
Window -> Preferences -> Web<br>
CSS Files/HTML Files/JSP Files -> Encoding : UTF-8<br><br>