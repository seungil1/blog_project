# Blog_Project

## 1. 목표와 기능

### 1.1 목표
<br />

* Django 이해 및 공부
* BLOG 기능 구현

<br />
  
### 1.2 기능
* 블로그 목록 조회: 등록된 블로그 목록을 표시하여 사용자가 선택할 수 있도록 함
* 블로그 상세 조회: 선택한 블로그의 상세 정보를 표시하여 사용자에게 제공
* 포스트 작성: 사용자가 블로그에 새로운 포스트를 작성할 수 있도록 함
* 포스트 수정 및 삭제: 사용자가 작성한 포스트를 수정하거나 삭제할 수 있도록 함
* 댓글 및 대댓글 작성: 사용자가 포스트에 댓글 또는 대댓글을 작성할 수 있도록 함
* 댓글 수정 및 삭제: 사용자가 작성한 댓글을 수정하거나 삭제할 수 있도록 함
* 즐겨찾기: 사용자가 좋아하는 포스트를 즐겨찾기에 추가하거나 제거할 수 있도록 함



## 2. 개발 환경 및 배포 URL
### 2-1 개발환경
- Visual Studio Code(Django)

### 2-2 URL구조

### register 앱

| App       | URL                | Views Function | HTML File Name           | Note              |
|-----------|--------------------|----------------|--------------------------|-------------------|
| register  | `/signup/`         | `user_signup`  | `register/signup.html`   | 회원가입 페이지    |
| register  | `/login/`          | `user_login`   | `register/login.html`    | 로그인 페이지      |
| register  | `/logout/`         | `user_logout`  | `register/logout.html`   | 로그아웃 처리      |
| register  | `/profile/`        | `user_profile` | `register/profile.html`  | 사용자 프로필 페이지 |

### post 앱

| App       | URL             | Views Function | HTML File Name        | Note                 |
|-----------|-----------------|----------------|-----------------------|----------------------|
| post      | `/`             | `post_list`    | `post/post_list.html` | 메인 페이지           |
| post      | `/create/`      | `post_create`  | `post/post_create.html`| 게시글 생성 페이지   |
| post      | `/<int:pk>/`    | `post_detail`  | `post/post_detail.html`| 게시글 상세 페이지   |
| post      | `/<int:pk>/update/` | `post_update`| `post/post_update.html`| 게시글 수정 페이지   |
| post      | `/<int:pk>/delete/` | `post_delete`| `post/post_delete.html`| 게시글 삭제 페이지   |

## WBS

```mermaid
graph TD;
    A[프로젝트 시작] --> B[요구사항 분석]
    B --> C[프로젝트 범위 정의]
    C --> D[일정 및 예산 결정]
    D --> E[팀 구성]
    E --> F[시작] 
    
    F --> G[프로젝트 설정]
    G --> H[데이터베이스 설계]
    G --> I[UI/UX 설계]
    G --> J[시스템 아키텍처 설계]
    J --> K[프로젝트 설정 완료]
    
    K --> L[사용자 관리 기능 구현]
    L --> M[회원가입 기능]
    L --> N[로그인 기능]
    L --> O[로그아웃 기능]
    L --> P[프로필 수정 기능]
    
    K --> Q[블로그 기능 구현]
    Q --> R[블로그 목록 조회 기능]
    Q --> S[블로그 포스트 조회 기능]
    Q --> T[포스트 작성 기능]
    Q --> U[포스트 수정 기능]
    Q --> V[포스트 삭제 기능]
    Q --> W[댓글 / 대댓글 생성 기능]
    Q --> X[댓글 삭제 기능]
    Q --> Y[댓글 수정 기능]
    Q --> Z[즐겨찾기 기능]
    Q --> AA[GPT 응답 기능]
    
    K --> AB[사용자 인증 및 권한 관리]
    AB --> AC[인증 데코레이터 구현]
    AB --> AD[권한 설정]
    
    K --> AE[테스트 및 디버깅]
    AE --> AF[단위 테스트]
    AE --> AG[통합 테스트]
    AE --> AH[시스템 테스트]
    
    K --> AI[서버 환경 설정]
    AI --> AJ[데이터베이스 마이그레이션]
    AI --> AK[웹 서버 배포]
    AI --> AL[보안 설정]
    AI --> AM[서비스 모니터링 및 유지보수 계획 수립]
