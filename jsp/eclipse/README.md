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

## .html -> .jsp 변환 시 한글 깨짐
.jsp [ALT]+[ENTER] -> Text file encoding -> Other : UTF-8 <br><br>
**코드블럭 추가**
```
<%@ page language="java" contentType="text/html; charset=UTF-8"
pageEncoding="UTF-8"%>
```
<br><br>
## JDBC(.jar 추가)
path : WEB-INF/lib/ojdbc8.jar

## View에서 사용하는 제어구조 - JSTL
JSTL(Jsp Standard Tag Library) <br>
JSTL.jar를 추가해야 사용할 수 있다<br>
https://mvnrepository.com/artifact/javax.servlet/jstl/1.2
<br><br>
JSTL을 사용하기 위해 View(.jsp)페이지에 코드 지시자 블럭을 추가<br>
```
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
```
<br><br>
## View(.jsp) 페이지 은닉
MVC모델은 실행순서가 Controller -> Model -> View순으로 이루어지는데 View(사용자 페이지)에 접근할 수 없도록 하는 방법<br>
/WEB-INF 폴더에 .jsp폴더를 위치시킨다<br>
ex) /WEB-INF/view(디렉터리 직접 생성)/.jsp <br><br>


## 페이지 에러
403(보안 오류) -> 권한이 없는 경우<br>
404(URL 오류) -> URL이 없는 경우<br>
405(메서드 오류) -> 메서드가 없는 경우(GET/POST)<br><br>



