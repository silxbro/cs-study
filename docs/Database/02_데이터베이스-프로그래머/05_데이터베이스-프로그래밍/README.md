# 데이터베이스 프로그래밍
<br/>

- 데이터베이스 프로그래밍의 개념을 이해한다.
- 저장 프로그램의 문법과 사용 방법을 알아본다.
- 자바 프로그램과 데이터베이스를 연동하는 방법을 알아본다.
- PHP 프로그램과 데이터베이스를 연동하는 방법을 알아본다.

SQL은 데이터베이스에 저장된 데이터를 다루는 최상의 언어이다. 하지만 데이터를 이용하는 응용 프로그램을 구축해야 할 경우 SQL만으로는 어렵다.
비행기가 하늘에서는 잘 날지만 육지에서는 다른 차의 도움을 받아 움직이듯이 SQL도 다른 언어의 도움이 필요하다.
이 장에서는 SQL 언어를 이용하여 프로그래밍하는 두 가지 방법을 배운다. 첫째, SQL 자체의 기능을 확장하여 프로그래밍 능력을 강화하는 방법이다.
이를 위해 각 DBMS는 전용 프로그래밍 언어(데이터베이스 프로그래밍 언어)를 제공하는데, MySQL에서는 저장 프로그램이라고 한다.
둘째, 자바, C++, JSP, PHP 등 일반 프로그래밍 언어의 도움을 받아 데이터는 SQL이, 응용 로직은 일반 프로그래밍 언어가 분담하여 해결하는 방법이다.
SQL과 일반 프로그래밍 언어와의 결합은 SQL 문을 일반 프로그램에 끼워 넣는 삽입(embeded) 방식으로 이루어진다.

### 01 : 데이터베이스 프로그래밍
DBMS에 데이터를 정의하고 시스템에 저장된 데이터를 읽어와 데이터를 변경하는 프로그램을 작성하는 과정을 말한다.
일반 프로그래밍과는 데이터베이스 언어인 SQL을 포함한다는 점이 다르다.

### 02 : 삽입 프로그래밍
데이터베이스 프로그래밍 방법 중 하나로 SQL을 자바, C와 같은 범용 프로그래밍 언어에 삽입하여 프로그래밍하는 것을 말한다.
SQL 문이 삽입된 자바, C와 같은 프로그래밍 언어를 호스트 언어라고 한다.

### 03 : 저장 프로그램
데이터베이스 전용 응용 프로그램을 작성할 때 사용하는 MySQL의 SQL 확장 언어이다.

### 04 : 저장 프로시저
저장 프로그램에서 사용하는 기능으로, 일반 프로그래밍 언어의 함수 대신 사용하는 명칭이다. 프로시저를 정의하여 DBMS에 저장한다.

### 05 : 커서
실행 결과 테이블을 한 번에 한 행씩 처리하기 위하여 테이블의 행을 순서대로 가리키는 데 사용하는 포인터를 말한다.
커서에 관련된 키워드로는 CURSOR, OPEN, FETCH, CLOSE 등이 있다.

### 06 : 트리거
데이터의 변경(삽입, 삭제, 수정)문이 실행될 때 자동으로 실행되는 프로시저다.
보통 트리거는 데이터 변경문이 처리되는 세 가지 시점, 즉 실행 전(BEFORE), 대신하여(INSTEAD OF), 실행 후(AFTER)에 동작한다.

### 07 : 연동
연동이란 어느 한 부분이 움직이면 다른 부분도 같이 움직인다는 의미로, 데이터베이스 응용에서는 일반 프로그램을 수행하여 DBMS를 동작시킨다는 의미이다.
연동은 자바 프로그램 혹은 웹 프로그램을 이용한다.

### 08 : JDBC
자바는 객체지향 언어이기 때문에 객체를 호출하여 데이터베이스에 접속한다. 데이터베이스에 접속하는 API(Application Programming Interface)를 java.sql.*에서 제공한다.
java.sql에 정의된 API는 각 DBMS 제조사에서 자신의 제품에 맞게 구현해서 제공하는데, 이를 JDBC(Java DataBase Connectivity) 드라이버라고 한다.