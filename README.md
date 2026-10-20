<div align="center">

# 안녕하세요, 백엔드 개발자 백승범입니다 👋

**운영 중인 서비스의 문제를 찾아서 직접 고치는 백엔드 개발자**를 목표로 하고 있습니다.<br/>
Spring Boot 기반 API 설계부터 인증/인가, Docker 배포와 CI/CD까지 서비스 전체 흐름을 경험하고 있습니다.

[![Email](https://img.shields.io/badge/Email-seungbeom1234@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:seungbeom1234@gmail.com)
<!-- 블로그나 포트폴리오가 있으면 여기에 배지를 추가하세요 -->

</div>

---

## 🛠 Tech Stack

**Backend**<br/>
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white)

**Database / Cache**<br/>
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Infra / DevOps**<br/>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)

**Frontend (협업 가능)**<br/>
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

---

## 🚀 Main Projects

### 1. H-CodeLab — 대학 수업용 코딩 실습·자동 채점 플랫폼
> 🏢 [2026-codelab](https://github.com/2026-codelab) · 2025.09 ~ 진행 중 · 🌐 [서비스 바로가기](http://ai.walab.info)

수업·과제·코딩 테스트를 운영하고, 학생이 제출한 코드를 **DOMjudge**와 연동해 자동 채점하는 서비스입니다. 실제 수업에서 운영 중입니다.

`Spring Boot` `JWT` `OAuth2` `MariaDB` `Redis` `DOMjudge` `Docker Compose` `Jenkins`

**담당 역할: 백엔드 기능 개발, 운영 이슈 해결, 서버 배포 (FE 연동까지 맡음)**
- **코딩 실습 기능**: 과제와 상관없이 코드를 실행해 볼 수 있는 실습 API를 새로 설계하고 개발
- **수업별 언어 제한**: 수업을 만들 때 사용 언어를 고르고, 그 언어로만 제출할 수 있도록 검증 로직 추가
- **단계별 힌트 생성 기능** 개발 (BE API + FE UI)
- **시스템 관리자 권한 관리**: 사용자 역할 수정 API와 관리 화면 구현
- **장애 수정**
  - 읽음 기록이 있는 수업을 삭제할 때 생기던 **FK 제약 오류** 해결
  - 비로그인 상태에서 `/api/user/me`를 호출하면 발생하던 **NPE** 수정
  - 인증에 실패했을 때 400 대신 **401을 반환**하도록 에러 응답 정리
  - 목록 API가 **중복 호출**되면서 간헐적으로 400이 나던 문제 해결
- **배포**: 새 서버로 옮기면서 Docker 기반 배포 설정을 구성하고, Jenkins 자동 배포 파이프라인을 운영
- 이슈 → PR → 코드 리뷰 흐름으로 협업 (PR 20건 이상 머지, 리뷰 참여)

📂 [Backend](https://github.com/2026-codelab/H-CodeLab_BE) · [Frontend](https://github.com/2026-codelab/H-CodeLab_FE) · [Deploy](https://github.com/2026-codelab/H-CodeLab_Deploy)

---

### 2. HiSign — 전자서명 기반 온라인 문서 관리 시스템
> 🏢 [Signify2](https://github.com/Signify2) · 2026.03 ~ 2026.06 · 캡스톤디자인

WA Lab의 전자서명 서비스를 이어받아 **기존 운영 서비스를 개선**한 프로젝트입니다.

`Spring Boot` `JPA` `React`

**담당 역할: 백엔드 기능 개선**
- 문서 유형을 문자열 대신 **Enum으로 관리**하도록 바꾸고, 그에 맞춰 입력 검증과 메서드 구조 정리
- 작업 유형 선택(radio) 기능 추가
- 과제·과목 기준 데이터를 최신 상태로 갱신
- 이슈 단위 브랜치(`feat/{issue}-...`)와 PR 머지 방식으로 협업

📂 [Backend](https://github.com/Signify2/HiSign-backend) · [Frontend](https://github.com/Signify2/HiSign-front)

---

## 🧩 Personal Projects

| 프로젝트 | 설명 | 기술 |
|---|---|---|
| [**PawCheck**](https://github.com/BackSeungBeom/PawCheck) | 한국관광공사 OpenAPI의 반려동물 출입 규정을 체크리스트로 바꾸고, 내 반려동물이 입장할 수 있는지 미리 알려주는 서비스 (2026 관광데이터 활용 공모전 출품). 규칙 기반 파서와 LLM 파싱을 함께 쓰고, 시설 937곳 데이터를 동기화. API 키가 없을 때 동작할 fallback도 설계 | Next.js, TypeScript, Prisma, LLM API |
| [**HGraduate**](https://github.com/BackSeungBeom/HGraduate_SpringBoot) | 학생의 이수 내역을 바탕으로 졸업 요건 충족 여부를 진단하는 서비스의 백엔드 | Spring Boot, JPA, MySQL, Docker Compose |
