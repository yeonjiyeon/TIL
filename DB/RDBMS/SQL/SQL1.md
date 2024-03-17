# SQL1

## 데이터베이스 언어

### ▪데이터베이스언어의필요

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/1b49505f-7f56-461a-81cc-471187fedece/Untitled.png)

데이터를 직접 수정, 삭제 할 수 없기 때문에 데이터베이스에게 명령할 명령어가 필요

### ▪SQL의개요

1. **SQL(Structured Query Language)은 관계대수에 기초하여 RDBMS의 데이터 관리를 위해 설계된 언어**
2. **1986년 ANSI, 1987년 ISO에서 표준으로 제정**
▶ SQL-86, SQL-89, SQL-92, SQL:1999, SQL:2003, SQL:2008
▶ 상용 DBMS의 특성에 맞게 국제표준을 확장한 독자적 버전이 존재
3. 특징
▶ 비절차적(선언형) 언어→ 관계대수와의 차이, 필요한 데이터만 기술
▶ 인간의 언어와 매우 유사하고 간단, 명료

### ▪SQL의구성

1. **데이터 정의 언어(DDL: Data Definition Language)**
▶ 데이터베이스 내의 객체를 생성 및 삭제하고 그 구조를 조작하는 명령어의 집합
▶ 데이터가 준수해야 하는 제약조건을 기술
▶ CREATE, ALTER, DROP 문 등
2. **데이터 조작 언어(DML: Data Manipulation Language)**
▶ DDL에 의해 정의된 테이블에 데이터를 조작하는 명령어의 집합
▶ 데이터에 대한 CRUD(생성, 검색, 삭제, 수정) 명령을 포함
▶ INSERT, UPDATE, DELETE, SELECT 문 등

## 데이터 정의 언어

### ▪데이터정의언어의개념

1. **데이터베이스 객체를 생성, 삭제 또는 구조를 수정하는 명령어의 집합**
2. **데이터베이스 객체의 종**류
▶ 데이터 저장 – 테이블, 인덱스, 뷰
▶ 데이터 조작 - 트리거, 프로시저, 함수 등
3. **데이터 정의 명령어의 종류**
▶ CREATE - 객체 생성
▶ ALTER - 객체 수정
▶ DROP - 객체 삭제

**데이터 정의 언어의 구문 형식**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/efc133ab-c495-4110-8c47-3571e88cf72d/Untitled.png)

### ▪스키마 정의

1. **스키마 = 데이터베이스(데이터의 집합)**
2. **한 조직의 데이터베이스 시스템의 운영에 필요한 테이블, 인덱스, 뷰 등의 데이터베이스 객체의 집합**
3. **스키마 관리 방법**
▶ Forward Engineer
▶ SQL 에디터
▶ 내비게이터 패널

**스키마 관리 구문 형식**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/ec11ee4f-600c-43ac-b9e2-267c0400ce60/Untitled.png)

### ▪테이블 정의, 수정, 삭제

**테이블 정의**

1. 새로운 2차원 형태의 테이블을 생성

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/5acff179-25a6-4b11-a8a4-f77aa7305321/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/68aa142a-1a29-4e97-a247-fe1b8d0696c3/Untitled.png)

**데이터 타입의 개념**

1. 컬럼이 가질 수 있는 값의 범위, 즉 도메인을 결정
2. 프로그래밍 언어에서의 변수를 생성하는 데이터 타입의 사용 목적과 방법이 매우 유사
3. 기본 데이터 타입

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/6d1c0d6c-3ab8-4884-8a17-8e00d4c63c36/Untitled.png)

**정수 데이터 타입**

1. TINYINT – 1바이트 정수, -128 ~ 127
▶ 나이, 학년 등의 크기가 작은 정수
2. SMALLINT – 2바이트 정수, -32768~32767
▶ 물품번호, 인원 등 중간 크기의 정수
3. INT – 4바이트 정수, 약 -20억 ~ 20억
▶ 물품의 금액, 전화번호 등의 일반 크기의 정수
4. BIGINT – 8바이트 정수
▶ 계좌의 잔고, 천문학적인 크기의 정수

**실수 데이터 타입**

1. 고정 소수형
▶ DECIMAL(M, N) – 전체 M 자리, 소수점 이하 N자리의 숫자를
• 예, DECIMAL(5,2)는 -999.99~999.99
▶ NUMERIC – DECIMAL과 동일
2. 부동 소수형
▶ FLOAT – 4바이트 크기 부동 소수
▶ FLOAT(P) – 소수점 이하 P개 자리의 부동 소수
▶ DOUBLE – 8바이트 크기 부동 소수형

**날짜 및 시간 데이터 타입**

1. 날짜 데이터 타입
▶ DATE – ‘YYYY-MM-DD’ 형식의 시간
▶ YEAR – ‘YYYY’ 형식의 연도
2. 시간 데이터 타입
▶ TIME – ‘HH:MI:SS’ 형식의 시간
3. 날짜 및 시간 데이터 타입
▶ DATETIME – ‘YYYY-MM-DD HH:MI:SS’
형식의 날짜 및 시간
▶ TIMESTAMP – DATETIME과 동일

**문자 데이터 타입 → 약 4000자까지 길이 지정 가능**

1. CHAR(N) – 최대 길이가 N인 고정길이 문자열
2. VARCHAR(N) – 최대 길이가 N인 가변길이 문자열
3. ‘DATABASE’ 문자열 저장 시

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/b3effd08-9b8c-40a3-8f69-9e62ce9f7d67/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/5d5c3d15-b4bb-4038-a811-9ef6763bd7ac/Untitled.png)

가변적으로 데이터가 변하면 속도가 느려 질 수 있기 때문에 VARCHAR가 무조건 좋다고 할 수 없다.

**문자 데이터 타입**

1. TEXT, CLOB – 길이가 최대 2~4GB인 가변 길이 문자열
2. ENUM – 유한 개의 문자열 집합 중 하나의 값을 선택
▶ 성별 – ENUM(‘남’, ‘여’)
▶ 혈액형 – ENUM(‘A’, ‘B’, ‘O’, ‘AB’)

**테이블 수정**

1. 생성된 테이블에 컬럼을 추가, 수정(이름, 데이터 타입, 제약조건) 또는 삭제하는 명령
2. 컬럼 삭제 또는 컬럼의 데이터 타입 수정 시 데이터에 대한 소실이 발생하므로 많은 주의가 요구
3. 테이블 수정 방법
▶ SQL 구문
▶ 내비게이터 패널

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/a2cd467b-92c1-4a65-9513-945db942c4e1/Untitled.png)

테이블 사용의 질의 사용

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/09adac38-629a-49bc-b209-f84429f4f48f/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/b661ef7a-0128-413c-a97e-e9155ca7223f/Untitled.png)

**테이블 삭제**

1. 존재하는 테이블을 스키마에서 삭제
2. 삭제할 테이블의 모든 데이터가 소실, 복구가 불가능 연산이므로 각별한 주의가 요구
3. 테이블 삭제 방법
▶ SQL 구문
▶ 내비게이터 패널

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/7ee88c41-640b-46e0-bdb2-c147928f34d1/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/69b5fa34-6ec4-425c-bf8c-810db816c0a9/Untitled.png)

### ▪제약조건

1. 테이블과 테이블에 존재하는 데이터를 보다 무결하게 관리하기 위한 목적으로 사용
2. DBMS는 테이블 조작 시 테이블에 정의된 제약조건을 만족시키는지 지속적으로 검사
3. DBMS는 적용하려는 제약의 유형에 따라 다양한 제약 조건을 지원

**제약조건의 종류**

1. PRIMARY KEY: 기본키 지정, UNIQUE와 NOT NULL 특성
2. FOREIGN KEY: 외래키 지정, 참조 컬럼 정의
3. NOT NULL: NULL이 될 수 없는 컬럼에 지정
4. UNIQUE: 동일한 컬럼값을 가질 수 없음을 지정
5. AUTO_INCREMENT: 레코드가 추가될 때 자동적으로 속성값이 1부터 1씩 증가되어 입력
6. CHECK: 컬럼 값이 특정 조건 준수 여부 지정

**제약조건의 사용**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/7e183dfb-ce68-4072-a853-3e6f112ecb75/Untitled.png)

**제약조건의 응용**