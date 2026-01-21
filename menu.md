# 📌 코딩 학습 LMS 메뉴 구조도 (URL 구조 기준 반영)

## 🟦 공통 메뉴 (비로그인 / 로그인 공통)

* 홈 (`/`)
* 강좌 목록 (`/courses`)

  * 레벨별 강좌

    * 입문 (`/courses/level/beginner`)
    * 초급 (`/courses/level/basic`)
    * 중급 (`/courses/level/intermediate`)
    * 고급 (`/courses/level/advanced`)
* 커뮤니티 (`/community`)
* 공지사항 (`/notices`)
* 로그인 / 회원가입

  * 로그인 (`/auth/login`)
  * 회원가입 (`/auth/register`)
  * 소셜 로그인 (`/auth/oauth`)

---

## 🟩 수강생 메뉴

*(기본 활성 역할)*

🔄 **역할 전환**

* 강사 화면으로 이동
  *(강사 역할 보유 + 승인 완료 시 노출)*

---

### 1️⃣ 대시보드

* 나의 레벨
* 학습 진행 현황
* 출석 현황
* 시험 응시 가능 상태
* 알림 요약
  ➡ `/student/dashboard`

---

### 2️⃣ 내 강좌

* 전체 내 강좌 (`/student/courses`)
* 수강 중 강좌 (`/student/courses/active`)
* 수강 완료 강좌 (`/student/courses/completed`)
* 수강 예정 강좌 (`/student/courses/planned`)

#### 강좌 상세

* 강좌 정보 (`/student/courses/{courseId}`)
* 강의 목록 (`/student/courses/{courseId}/lectures`)
* 강의 시청 (`/student/lectures/{lectureId}`)
* **수강 신청** (`/student/courses/{courseId}/enroll`)
* **수강 취소** (`/student/courses/{courseId}/cancel`)
* Q/A 바로가기

---

### 3️⃣ 코딩 연습

* 실습 문제 목록 (`/student/practice`)
* 레벨별 문제 (`/student/practice/level/{level}`)

#### 문제 상세

* 문제 설명
* 코드 작성
* 실행 / 제출 (`/student/practice/{problemId}/submit`)
* 결과 확인

---

### 4️⃣ 시험 / 평가

* 시험 목록 (`/student/exams`)
* 레벨업 시험 (`/student/exams/levelup`)
* 시험 응시 (`/student/exams/{examId}`)
* 시험 결과 (`/student/exams/{examId}/result`)

  * 점수
  * 오답 요약
  * 재응시 가능 시점

---

### 5️⃣ 출석 / 이력

* 출석 기록 (`/student/attendance`)
* 학습 로그 (`/student/history`)
* 시험 응시 이력 (`/student/history/exams`)

---

### 6️⃣ 결제 / 수강권

* 결제 내역 (`/student/payments`)
* 크레딧 현황 (`/student/payments/credits`)
* 수강권 구매 (`/student/payments/purchase`)
* 환불 내역 (`/student/payments/refunds`)

---

### 7️⃣ Q/A

* 내 질문 목록 (`/student/qna`)
* 질문 등록 (`/student/qna/new`)
* 질문 상세 (`/student/qna/{id}`)

---

### 8️⃣ 알림

* 알림 목록 (`/student/notifications`)

---

### 9️⃣ 설정

* 회원 정보 수정 (`/student/settings/profile`)
* 비밀번호 변경 (`/student/settings/password`)
* 로그아웃

---

## 🟨 강사 메뉴

*(강사 역할 활성 시)*

🔄 **역할 전환**

* 학습자 화면으로 돌아가기

---

### 1️⃣ 강사 대시보드

* 개설 강좌 현황
* 수강생 수
* 수익 요약
* 승인 상태
  ➡ `/instructor/dashboard`

---

### 2️⃣ 강좌 관리

* 강좌 목록 (`/instructor/courses`)
* 강좌 개설 요청 (`/instructor/courses/new`)
* 강좌 상세 (`/instructor/courses/{id}`)
* 강의 업로드 요청 (`/instructor/lectures/upload`)
* 강의 관리 (`/instructor/lectures`)

---

### 3️⃣ 과제 관리

* 과제 목록 (`/instructor/assignments`)
* 과제 등록 (`/instructor/assignments/new`)
* 과제 상세 (`/instructor/assignments/{id}`)

---

### 4️⃣ Q/A 관리

* 질문 목록 (`/instructor/qna`)
* 답변 등록 / 수정 (`/instructor/qna/{id}`)

---

### 5️⃣ 수익 / 정산

* 정산 내역 (`/instructor/settlement`)
* 계좌 정보 관리 (`/instructor/account`)

---

### 6️⃣ 알림

<<<<<<< HEAD
* 승인 결과 알림
* Q/A 알림
=======
* 강사 알림 (`/instructor/notifications`)
## 🟥 관리자 메뉴
### 1️⃣ 관리자 대시보드

<<<<<<< HEAD
* 전체 통계 요약
* 매출 현황
* 사용자 현황
=======
➡ `/admin/dashboard`
>>>>>>> sub

---

### 2️⃣ 회원 관리

<<<<<<< HEAD
* 수강생 관리
* 강사 관리
* 계정 제한 / 정지
=======
* 전체 회원 (`/admin/users`)
* 수강생 관리 (`/admin/users/students`)
* 강사 관리 (`/admin/users/instructors`)
>>>>>>> sub

---

### 3️⃣ 강좌 / 강의 관리

<<<<<<< HEAD
* 강좌 승인 / 반려
* 강의 승인 / 반려
* 강의 수정 / 삭제
=======
* 강좌 관리 (`/admin/courses`)
* 승인 대기 강좌 (`/admin/courses/pending`)
* 강좌 승인 / 반려
* **강좌 모집 종료** (`/admin/courses/{id}/close`)
* 강의 관리 (`/admin/lectures`)
* **강의 비활성화** (`/admin/lectures/{id}/inactive`)
>>>>>>> sub

---

### 4️⃣ 결제 / 환불 관리

<<<<<<< HEAD
* 결제 내역 조회
* 환불 처리
=======
* 결제 내역 (`/admin/payments`)
* 환불 처리 (`/admin/refunds`)
>>>>>>> sub

---

### 5️⃣ 커뮤니티 관리

<<<<<<< HEAD
* 게시글 관리
* 신고 처리
* 제재 이력
=======
* 게시글 관리 (`/admin/community`)
* 신고 처리 (`/admin/reports`)
>>>>>>> sub

---

### 6️⃣ 시험 / 평가 관리

<<<<<<< HEAD
* 시험 문제 관리
* 채점 기준 관리
* 레벨 기준 설정
=======
* 시험 관리 (`/admin/exams`)
* 시험 문제 관리 (`/admin/exams/questions`)
>>>>>>> sub

---

### 7️⃣ 로그 / 이력 관리

<<<<<<< HEAD
* 출석 로그
* 수강 로그
* 시험 로그
* 승인 이력
=======
* 로그 조회 (`/admin/logs`)
* 출석 로그 (`/admin/logs/attendance`)
* 시험 로그 (`/admin/logs/exams`)
>>>>>>> sub

---

### 8️⃣ 공지사항 관리

<<<<<<< HEAD
* 공지 등록 / 수정
* 댓글 관리
=======
* 공지 관리 (`/admin/notices`)
>>>>>>> sub

---

### 9️⃣ 알림 관리

<<<<<<< HEAD
* 알림 템플릿 관리
* 발송 이력

---

## 🧠 메뉴 구조 한 줄 요약

> **수강생 = 학습 중심**
> **강사 = 콘텐츠 & 수익 중심**
> **관리자 = 승인 & 운영 중심**

---

## 📌 평가자 시점에서 좋은 이유

* 기능 정의서와 1:1 매칭됨
* 역할별 메뉴 분리 명확
* “보완 필수” 항목 전부 위치 있음
* 실제 서비스랑 구조 동일

---
=======
* 알림 관리 (`/admin/notifications`)

---

## 🧠 최종 한 줄 정리

> **메뉴 명칭과 URL이 1:1로 대응되도록 정리되어,
> 설계–구현–발표 간 괴리가 없는 구조**
>>>>>>> sub
