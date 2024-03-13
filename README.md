# Blog_Project

## 1. 목표와 기능

### 1.1 목표

* Django 이해 및 공부
* BLOG 기능 구현
  
### 1.2 기능



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
