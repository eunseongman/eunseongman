# 👋 데이터 정합성과 성능 최적화를 중시하는 개발자, 이은성입니다

> **500일 이상 연속 알고리즘 문제 풀이**  
> **SSAFY 13기 우수 교육생**  
> 실행 구조를 근거로 병목을 분석하고, 측정 가능한 개선으로 시스템 품질을 높이는 개발자입니다.

---

## 🧩 About Me

- **PostgreSQL 실행 계획 분석과 쿼리 튜닝으로 검색 API 응답 시간을 4.21초에서 0.123초까지 개선했습니다.**  
  PostgreSQL `JSON → JSONB` 전환, `GIN 인덱스` 적용, 실행 계획 분석을 바탕으로 병목 구간을 줄였습니다.

- **PCB 협업 시스템을 웹 기반으로 전환해 열 해석 모델링 준비 시간을 40시간에서 1시간으로 단축했습니다.**  
  Excel·Visio 기반 수작업 프로세스를 서버 중심 구조로 바꾸며 변경 이력 관리와 재사용성을 높였습니다.

- **500일 이상 알고리즘 문제를 꾸준히 풀며 문제 해결력과 기본기를 유지해왔습니다.**  
  구현, 탐색, 자료구조, 최적화 문제를 지속적으로 다루며 안정적인 사고력을 쌓아왔습니다.
  
---

## 🛠 Tech Stack

| Category | Tech & Tools |
|:---|:---|
| **Language** | `Java 8,17`, JavaScript, SQL |
| **Backend** | `Spring Boot`, Spring Security, JDBC Template, MyBatis, `JPA`, `Spring Data JPA` |
| **Frontend** | Vue.js |
| **Database** | MySQL, `PostgreSQL` |
| **DevOps / Tools** | Docker, Git, Jira, Notion |

---

## 🚀 Major Projects

### 🔹 PCB Collaboration Tool (삼성전자 네트워크사업부 연계)
**기간:** 2025.08 ~ 2025.11  
**인원:** 6명 (BE 2 / FE 4)  
**역할:** Backend 70%, Frontend 20%

- **문제**  
  각 설계팀이 Visio·Excel 기반으로 개별 작업한 뒤 메일과 구두로 수동 취합하던 구조였습니다. 변경 이력 관리가 어렵고, 기존 배치 데이터를 재사용하기도 어려워 열 해석 모델링 준비에 많은 시간이 들었습니다.

- **내 역할**  
  웹 기반 단일 협업 환경의 백엔드를 맡아 REST API 구현, 부품 배치 버전 관리 ERD 설계, 라이브러리 기능 구현, 검색 API 성능 개선, API 명세 작성과 일정 관리를 담당했습니다.

- **핵심 개선**
  - 부품 배치부터 열 해석 모델링 산출까지 단일 통합 환경으로 전환
  - 기존 배치 데이터를 재사용할 수 있는 라이브러리 기능 구현
  - PostgreSQL `JSON → JSONB` 전환 및 `GIN 인덱스` 적용
  - 실행 계획 분석 후 `LIMIT ? → LIMIT 5`로 변경해 Top-N Sort 유도

- **성과**
  - 열 해석 모델링 준비 시간 **40시간 → 1시간 (약 97.5% 단축)**
  - 검색 API 응답 시간 **4.21초 → 0.123초 (약 97.1% 감소)**
  - 400명 이상 실무자 대상 베타 테스트 및 공청회 피드백 반영

- **기술 포인트**  
  `Java 8`, `Spring Boot 2.7`, `PostgreSQL`, `JDBC Template`, `Vanilla JavaScript`
  
---

### 🔹 [TMI (Tech Mania’s Information)](https://github.com/techmaniasinformation)
**기간:** 2025.07 ~ 2025.08  
**인원:** 6명 (BE 3 / FE 3)  
**역할:** Backend 60%

- **문제**  
  기술 블로그를 직접 탐색할 수 있는 플랫폼을 만들면서, 인기 게시글을 짧은 주기로 갱신할 구조와 사용자에게 즉시 가깝게 알림을 전달할 구조가 필요했습니다. 또 단순 검증 실패까지 예외로 처리하는 구조 때문에 응답 기준도 일관되지 않았습니다.

- **내 역할**  
  Spring Boot 기반 REST API 구현을 맡았고, 인기 게시글 랭킹 구조, SSE 기반 실시간 알림, 응답 구조 개선을 중심으로 백엔드 로직을 설계했습니다.

- **핵심 개선**
  - 조회수·즐겨찾기·시간 감쇠를 반영한 인기글 점수 모델 설계
  - 10분 주기 Scheduler + Projection + Bulk Upsert로 DB I/O 감소
  - SSE 기반 실시간 알림 구조 구현, 이벤트 리스너로 비즈니스 로직과 전송 로직 분리
  - `ServiceResult<T>` 기반으로 비즈니스 실패와 시스템 예외를 분리
  - Redis Cache-Aside와 k6 부하 테스트로 조회 성능 검증

- **성과**
  - 인기 게시글 10분 주기 자동 갱신 구조 구현
  - 사용자 알림 **1초 이내 전달 구조** 구현
  - 조회 API p95 **357ms → 45ms (약 87.4% 감소)**
  - 평균 응답 시간 **99ms → 12ms (약 87.9% 감소)**
  - 처리량 **464 req/s → 652 req/s (약 40.5% 증가)**
  - SSAFY 공통 프로젝트 우수상 수상

- **기술 포인트**  
  `Java 17`, `Spring Boot 3`, `MySQL`, `Spring Data JPA`, `Redis`, `SSE`
  
---

### 🔹 [SSAFY FORCE – 알고리즘 랭킹 플랫폼](https://github.com/SSAFYFORCE)
**기간:** 2025.06 ~ 2025.08  
**인원:** 4명  
**역할:** Backend 30%, Frontend 30%

- **문제**  
  팀 가입 요청을 여러 관리자가 동시에 처리할 수 있는 구조라, 같은 요청에 대해 수락과 거절이 동시에 반영될 수 있었습니다. 이 경우 상태 충돌과 잘못된 후속 처리로 이어질 수 있었습니다.

- **내 역할**  
  팀 기능과 권한 관리 기능을 개발했고, 가입 요청 처리 구간의 정합성 문제를 해결했습니다.

- **핵심 개선**
  - `JPA @Version` 기반 낙관적 락 적용
  - 충돌 빈도가 낮고 읽기 비중이 높은 구조를 고려해 비관적 락 대신 낙관적 락 선택
  - 버전 충돌 시 `OptimisticLockException` 계열 예외를 감지해 요청을 실패 처리하고, 이미 다른 관리자가 처리한 요청이라는 메시지를 반환하도록 예외 처리 흐름을 구성


- **성과**
  - 동시 처리 상황에서 가입 요청 상태 충돌 방지
  - 팀 가입 요청 처리의 데이터 정합성 확보

- **기술 포인트**  
  `Spring Boot`, `JPA`, `MySQL`, `Vue.js`
  
---

## Troubleshooting Highlights

- **PostgreSQL JSONB + GIN 인덱스 + 실행 계획 분석으로 검색 API 응답 시간을 4.21초 → 0.123초로 줄였습니다.**  
  회로 데이터는 구조가 자주 달라 유연한 저장 방식이 필요했고, 내부 검색 성능을 위해 `JSON` 대신 `JSONB`, 포함 검색에 유리한 `GIN` 인덱스를 선택했습니다. 대신 `JSONB + GIN`은 쓰기 비용과 저장 공간이 늘어나는 trade-off가 있었으나, 검색 횟수가 쓰기 횟수보다 더 많았기 때문에, 해당 해결 방식을 선택했습니다.

- **Redis Cache-Aside + k6 부하 테스트로 조회 API의 p95를 357ms → 45ms로 줄이고 처리량을 40% 이상 높였습니다.**  
  인기 게시글은 같은 결과가 반복 조회되고 10분 주기로 다시 계산되는 구조라 `Cache-Aside`가 적합했습니다. 다중 인스턴스 환경과 조회 부하를 크게 줄일 수 있는 Redis 를 선택했습니다.

- **ServiceResult 기반 응답 구조로 비즈니스 실패와 시스템 오류를 분리했습니다.**  
  단순 검증 실패까지 예외로 처리하던 구조를 바꿔, 예상 가능한 실패는 `ServiceResult<T>`로 반환하고 시스템 장애만 Exception으로 남겼습니다. 모든 실패를 예외로 통일하는 방식보다 로그 오염을 줄이고 의도를 명확히 할 수 있었지만, CUD 트랜잭션에서는 롤백 처리 기준을 더 신중하게 설계해야 하는 trade-off가 있었습니다.

- **SSE 기반 실시간 알림으로 1초 이내 전달 구조를 구현했습니다.**  
  알림은 서버에서 클라이언트로 보내는 단방향 통신이 핵심이라, 양방향 통신인 WebSocket보다 구조가 단순한 `SSE`를 선택했습니다.

- **짧은 주기로 반복 실행되는 인기글 집계 작업에는 Spring Scheduler를 적용해 구현 복잡도를 낮췄습니다.**  
대신 다중 서버 환경에서는 작업이 중복 실행될 수 있고 실행 이력 관리도 약하다는 한계가 있어, 규모가 커지면 분산 락이나 Spring Batch 같은 별도 실행 구조가 필요합니다.

---

## 🏆 Awards 

| Date | Title | Organization |
|:---|:---|:---|
| 2025.10 | 삼성전자 연계 프로젝트 우수상 | Samsung SW Academy |
| 2025.08 | SSAFY 공통 프로젝트 우수상 | Samsung SW Academy |
| 2025.05 | SSAFY 1학기 성적 우수상 | Samsung SW Academy |
| 2024.02 | 청운대학교 총장상 (학과 수석) | Cheongwoon Univ. |

## 🪪 License

| Date | Title | Organization |
|:---|:---|:---|
| 2023.06 | 정보처리기사 | 한국산업인력공단 |
| 2023.12 | SQLD | 한국데이터산업진흥원 |

---

## 📖 Education

| Date | Title | Organization |
|:---|:---|:---|
| 2026.02 ~ | 한국경제신문 with TOSS BANK Tech 우수인재 양성 LLM 과정 (3기) | 한경 아카데미 |
| 2025.01~12 | 삼성 청년 SW·AI 아카데미 (SSAFY 13기) | 삼성전자 |
| 2018~2024 | 청운대학교 컴퓨터공학과 (4.43/4.5) | Cheongwoon Univ. |

---

## 🧠 Algorithm & Problem Solving

[![Solved.ac Profile](http://mazassumnida.wtf/api/generate_badge?boj=rkdmfqka)](https://solved.ac/rkdmfqka)

- **500일 이상 연속 알고리즘 문제 풀이**
- **삼성 SW 역량테스트(모의) A+ 등급**
- 꾸준한 문제 풀이를 통해 자료구조, 탐색, 구현, 최적화 역량을 지속적으로 강화하고 있습니다.

---

## 📫 Contact

- **Email**: tkdgus4744@naver.com
- **Solved.ac**: https://solved.ac/profile/rkdmfqka

---

## 📌 One More Thing

저는 기능을 빠르게 만드는 것보다,  
**왜 느린지**, **왜 깨질 수 있는지**, **어떻게 더 안정적으로 운영할 수 있는지**를 먼저 고민하는 개발자입니다.

앞으로도 실행 구조를 이해하고, 병목을 추적하고,  
측정 가능한 개선으로 시스템 품질을 높이는 백엔드 개발자로 성장하겠습니다.

