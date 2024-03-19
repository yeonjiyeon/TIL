## 데이터 삽입, 수정, 삭제

### ▪데이터조작언어의개념

1. DML: Data Manipulation Language
2. 정의된 테이블에 레코드를 삽입·수정·삭제 및 검색하는데 사용되는 명령어의 집합
3. 명령어의 종류
▶ INSERT – 테이블 스키마에 적합한 레코드를 삽입
▶ UPDATE – 테이블에서 조건을 만족하는 특정 레코드의 컬럼값을 수정
▶ DELETE – 테이블에 조건을 만족하는 특정 레코드를 삭제
▶ SELECT – 조건을 만족하는 레코드를 테이블에서 검색

### ▪ INSERT 문

1. 테이블에 새로운 레코드를 삽입하는 명령문
▶ 테이블에 새로운 레코드를 삽입
▶ 모든 속성 또는 부분 속성에 대한 속성값을 삽입

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/8a1e7d1a-b869-4445-af2b-de1e994621fb/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/ddf0399a-860c-4e6f-8cfb-614045cd795d/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/d8f69638-7815-4edb-aa41-a9d728d94b6e/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/00ed922a-fbb2-4ce9-9858-9fc75eb30c2c/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/207c3a68-e946-43cb-a1c2-ff23f4981daf/Untitled.png)

### ▪UPDATE 문

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/792c2bbc-c16d-49a6-b7ca-207980d6081a/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/70633030-7f38-4f29-b8db-c26376189e4f/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/3ba91d6d-b5a1-4137-9e04-8424cfba0b87/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/fe721781-a5b2-40ed-aecb-6aaaeea68f4c/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/57cc76cf-aed6-4651-b4b9-26b87c12d710/Untitled.png)

### ▪DELETE 문

1. 조건에 일치하는 레코드 집합을 테이블에서 삭제할 때 사용하는 명령어

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/f8030d84-157d-4534-9ac7-557cef6269b1/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/19dc213d-e2b3-4069-bd3f-01dcbae57c25/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/7a0abc14-7a18-4c69-a753-1e26f33fcf56/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/0cefb07f-bda4-4284-bf59-c6a11bdf9e32/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/ea55d1ba-74ef-492c-9a90-c51c45b25f86/Untitled.png)

### SAFE UPDATES 모드

1. WHERE절이 없는 UPDATE/DELETE 문은 테이블의 전체 레코드를 변경/삭제
2. 의도하지 않은 데이터 변경/삭제 방지를 위해 MySQL은 SAFE UPDATES 모드를 지원
3. 기본키가 아니 컬럼을 대상으로 수정/삭제 조건을 명시할 경우 실행 여부를 결정

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/eec84ea4-c22d-4e2c-88fa-101747118566/Untitled.png)

## 데이터 검색 (1)

### ▪SELECT 문

1. 한 개 이상의 테이블에서 주어진 조건에 만족하는 레코드를 출력하는 명령문
2. 관계 대수의 셀렉션, 프로젝션, 조인, 카티션 프로덕트 연산자의 기능을 모두 포함있는 명령문
3. 필수적 절인 SELECT 절과 부가적인 목적으로 사용할 수 있는 여러 절을 혼합하여 검색 기능을 구체화

### ▪SELECT 문구문형식

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/6984a934-40a5-4ec6-a145-cfdf50dbdca8/Untitled.png)

### SELECT 문의 각 절의 기능

1. SELECT 절 – 결과에 포함되는 컬럼을 지정
2. FROM 절 – 질의를 적용할 테이블을 지정
3. ON/WHERE 절 – 조인 조건/검색할 레코드 조건을 지정
4. GROUP BY 절 – 레코드를 그룹화하기 위한 그룹 조건을 지정
5. HAVING 절 – GROUP BY 절이 적용된 결과에 대한 조건을 지정
6. ORDER BY 절 – 검색 결과의 정렬 기준을 지정

### ▪단순질의문

1. 레코드를 제한하지 않고 전체 테이블을 검색하는 SELECT 문으로 WHERE 절이 없는 질의문

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/05e4f5bf-1d1e-4287-b73d-9665263923de/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/86f6f2a3-9b0a-4e71-b241-f23687b998ff/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/038104ae-8000-476d-91c1-e494b09e909f/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/5480a61f-ebf4-4eb1-b11e-dae8bd25c257/Untitled.png)

### ▪조건질의문

1. 산술연산식, 함수 등을 사용하여 표현한 조건을 WHERE 절에 기술하여 조건을 만족하는 레코드만 검색하는 SELECT 문
▶ 산술연산자
▶ 비교연산자
▶ 논리연산자
2. WHERE 절은 UPDATE, DELETE 문에서도 동일하게 적용

### ▪특수연산자

1. SELECT 절 또는 WHERE 절에 사용되어 컬럼값 또는 상수와의 산술 계산을 위한 연산자

**산술연산자**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/17edc868-b814-4e77-b484-3eb70434d473/Untitled.png)

**비교연산자**

1. 컬럼값과 상수 또는 컬럼값과 다른 컬럼값과의 크기를 비교하는 연산자

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/eb9cc030-9547-4ab3-84b2-980af828e238/Untitled.png)

**조건질의문의 사용**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/d7e44a06-a3d5-470d-a698-34c713b64287/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/bd629fb9-2dd5-46ff-8213-ade01b685663/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/ea31bbb2-145e-402e-9607-f60b8a41833b/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/1202c335-8bac-40ff-88ab-a0f55db07f01/Untitled.png)

**데이터 정렬**

1. ORDER BY 절을 사용
2. 검색 결과를 특정 컬럼에 대해 오름차순 또는 내림차순으로 정렬
▶ 오름차순: ASC
▶ 내림차순: DESC

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/6531b21b-206e-44bd-bf21-6f5d58b51b28/Untitled.png)

▪함수

특수연산자 

1. 범위 포함 여부, 부분 일치 여부, 포함 여부 등 관계형 데이터베이스에서만 사용되도록 고안된 연산자

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/843dea1e-9ee5-4660-b7d5-c49f782187cc/7bf1867c-c118-4587-8215-7b3b86952996/Untitled.png)