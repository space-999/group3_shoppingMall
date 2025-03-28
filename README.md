# **신사 숙녀 쇼핑몰**
### 📖 프로젝트 개요 (Overview / Description)

- **20, 30대를 위한 깔끔하고 트랜디**한 UI/UX를 제공하는 **의류 쇼핑몰**
- 벤치마킹 쇼핑몰: **무신사 스토어** (https://www.musinsa.com/main/musinsa/recommend)
- 무신사처럼 **온라인 패션 스토어**이며, **자체 상표 브랜드**
- **모던/베이식/캐주얼**한 의류 제품을 공장에서부터 **입고, 진열, 관리, 판매, 배송, 고객 관리** 등을 한 번에 관리할 수 있는 **자체 쇼핑몰**
- **다양한 구매 방식**을 제공해 **사용자 만족도**를 높임

### 🛠️ 기술 스택 (Tech Stack)

- Java 21
- Spring Boot 3.x
- MySQL 8.0.41
- MyBatis

### ✅ 진행 상황 (progress)

1. **프로젝트 구현 및 실행 조건** - 2025.03.10 ~ 2025.03.16 (완)
    - ERD툴을 이용한 논리 모델링 작성
    - 물리 모델링 & 테이블 생성 및 데이터 입력 스크립트 작성
    - MySQL8.x 데이터 베이스에 물리 모델 구축
2. **서비스 구현** - 2025.03.16 ~ 2025.03.19 (완)
    - 기술 버전 결정
    - 각자 화면 정의서, 요구사항 정의서, 기술 정의서를 바탕으로 각 파트 구현
3. **테스트** - 2025.03.20 ~ 2025.03.28 (완)
    - 각자 개발한 파트 유닛 테스트 진행
    - 원활한 사용자 UX를 위해 예외 처리
    - 전체적인 흐름에서 부터 세부적인 흐름으로 들어가면서 정의서와 맞게 구현되어 있는지 체크
4. **발표 자료 정리 및 준비** - 2025.03.28 ~ 2025.03.30 
    - 각자 개발한 서비스 정리
    - 흐름도 정리
    - README.md 업데이트
5. **발표** - 2025.03.31
    - 본인 파트 발표 및 Q&A
6. **리팩토링 및 Spring/JPA 변환** - 2025.04.01 ~ 2025.04.30
    - Spring boot, MyBatis 를 Spring 으로 변환해보기 (선택)


### 📂 폴더 구조 (Optional but helpful)
- **src/main**
  - **/java/org/example/shoppingmall** : 구현한 JAVA 파일들이 저장되는 구조
    - /config : 설정 관련 클래스
    - /controller : 클라이언트 요청을 처리하는 컨트롤러
    - /dto : 요청 및 응답을 위한 DTO
    - /repository : DB 접근을 담당하는 인터페이스
    - /service : 비즈니스 로직을 처리하는 서비스 클래스
    - 각 폴더마다 자신이 맡은 파트(complaint, user, order, payment, product, shipping)
  - **/resources** :
    - /mapper
    - /mybatis
    - /static
      - /assets
      - /css
      - /images
      - /js
    - /templates
      - /

### 🚀 시작 방법 (Getting Started)
1. Clone the repository
2. git clone https://github.com/kimyelin0506/KDT_DBE3_Toy_Project1.git
3. Setup DB and environment
4. Run the application

### 👤 팀원 소개 (Optional)

#### *ERD 설계 담당 파트를 기준으로 개발 또한 관련 파트로 나눔*

- 김우주: **[주문]** 관련 파트
- 김예린: **[상품]** 관련 파트
- 김예지: **[배송]** 관련 파트
- 문지환: **[결제]** 관련 파트
- 이병우: **[취소/교환/환불]** 관련 파트
- 이민형: **[고객], [장바구니]** 관련 파트

### 📌 주요 기능 (Features)

1. **고객**
    - **구매자**
        - 로그인
        - 회원가입 기능
        - 마이페이지 기능
        - 장바구니
    - **관리자**
        - 직원 관리
2. **상품**
    - **구매자**
        - 상품을 정렬/필터링하여 쇼핑
        - 상품의 상세 정보를 제공 받음
    - **관리자**
        - 상품 입출고, 각 상품마다의 상태(진열 여부) 변경 및 관리
        - 상품의 상세 정보 수정
        - 리퍼/교환/폐기 상태 관리 및 처리
        - 시즌 및 할인 관리
3. **주문**
    - **구매자**
        - 상품 주문 기능
        - 상품주문 목록 확인
        - 상세 주문 확인
        - 전체 주문 이력 확인
4. **결제**
    - 결제시 결제수단 및 현금영수증 정보 입력
    - 매출전표 및 거래명세서 출력 가능
5. **배송**
    - **구매자**
        - 배송 정보 확인 및 배송 현황 조회
    - **판매자**
        - 계약 업체 직원들 정보 관리
        - 배송 건에 대한 수거 및 발송 관리
        - 발송한 상품에 대한 상태 관리
        - 교환&환불 건에 대한 상태 관리
6. **취소/환불/교환**
    - **구매자**
        - 취소,환불,교환 각각의 유형에 맞는 민원 신청 및 확인
        - 민원 유형에 맞는 자주 하는 질문 확인 가능
    - **관리자**
        - 고객이 신청한 민원 유형에 따라 처리 및 관리
        - 민원 처리 상태에 따라 이력 확인 가능
        - 민원 유형에 따라 고객들이 자주 하는 질문, 답변 작성 및 관리
