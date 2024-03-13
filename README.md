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
graph TD;
 A --> A1
    A --> A2
    A --> A3
    A --> A4
    A --> A5
    A1 --> B
    A2 --> B
    A3 --> B
    A4 --> B
    A5 --> B
    B --> B1
    B --> B2
    B --> B3
    B1 --> C
    B2 --> C
    B3 --> C
    C --> C1
    C --> C2
    C --> C3
    C --> C4
    C --> C5
    C --> C6
    C1 --> D
    C2 --> D
    C3 --> D
    C4 --> D
    C5 --> D
    C6 --> D
    D --> D1
    D --> D2
    D --> D3
    D1 --> E
    D2 --> E
    D3 --> E
    E --> E1
    E --> E2
    E --> E3
    E1 --> F
    E2 --> F
    E3 --> F
    F --> F1
    F --> F2
    F --> F3
    F --> F4
    F1 --> G
    F2 --> G
    F3 --> G
    F4 --> G
    G --> G1
    G --> G2
    G --> G3
