# Blog_Project

## 1. 목표와 기능

### 1.1 목표
<br />

* Django 이해 및 공부
* BLOG 기능 구현

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
gantt
    title 장고 블로그 프로젝트 개발 일정
    dateFormat  YYYY-MM-DD
    section 프로젝트 기획
        요구사항 분석      :2024-01-01, 7d
        기능 명세 작성    :2024-01-08, 5d
        데이터베이스 모델링:2024-01-15, 5d
        UI/UX 설계       :2024-01-22, 5d
        프로젝트 일정 수립:2024-01-29, 3d

    section 환경 설정
        가상 환경 설정    :2024-02-01, 3d
        Django 설치      :2024-02-04, 2d
        프로젝트 생성    :2024-02-06, 2d

    section 기본 기능 구현
        사용자 인증 시스템 구현:2024-02-08, 7d
        블로그 모델 생성      :2024-02-15, 5d
        블로그 CRUD 기능 구현 :2024-02-22, 7d
        댓글 기능 구현         :2024-02-29, 5d
        카테고리 및 태그 구현 :2024-03-06, 5d
        검색 기능 구현         :2024-03-13, 5d

    section 프론트엔드 개발
        템플릿 작성          :2024-03-20, 5d
        CSS 스타일링         :2024-03-27, 5d
        JavaScript 추가 기능 구현:2024-04-03, 7d

    section 테스트 및 디버깅
        기능 테스트            :2024-04-10, 5d
        디버깅 및 버그 수정    :2024-04-17, 5d
        보안 검토              :2024-04-24, 3d

    section 배포
        서버 구축               :2024-04-27, 5d
        배포 설정               :2024-05-02, 3d
        데이터베이스 마이그레이션:2024-05-05, 2d
        프로젝트 라이브 배포   :2024-05-07, 2d

    section 유지 보수 및 업데이트
        사용자 피드백 수집     :2024-05-09, 7d
        버그 수정 및 업데이트 :2024-05-16, 5d
        추가 기능 개발 및 배포 :2024-05-23, 7d
