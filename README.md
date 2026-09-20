# TeamMate

**대학교 팀 프로젝트 모집을 위한 Node.js 백엔드**

`JavaScript` · `Express` · `Firebase Authentication` · `Firestore`

소프트웨어공학 팀 프로젝트의 백엔드 개발 기록입니다. 회원·프로필, 모집 게시글, 프로젝트 지원서와 채팅 API를 구현했습니다.

## 코드 둘러보기

| 기능 | 라우트 | 컨트롤러 |
| --- | --- | --- |
| 회원·프로필 | [authRoutes](src/routes/authRoutes.js) | [authController](src/controllers/authController.js) |
| 게시글 | [postRoutes](src/routes/postRoutes.js) | [postController](src/controllers/postController.js) |
| 지원서 | [applicationRoutes](src/routes/applicationRoutes.js) | [applicationController](src/controllers/applicationController.js) |
| 채팅 | [chatRoutes](src/routes/chatRoutes.js) | [chatController](src/controllers/chatController.js) |

## 실행 조건

현재 실행 진입점은 `src/app.js`입니다. `package.json`에는 `start` 스크립트가 없으며, 자동 테스트도 아직 구성되지 않았습니다.

```bash
git clone https://github.com/InaJeong73/TeamMate.git
cd TeamMate
npm ci
node src/app.js
```

실행 전 본인의 개발용 Firebase 프로젝트와 자격증명 구성이 필요합니다. 저장소에 기록된 기존 서비스 계정 키는 재사용하지 않습니다. 비밀키 폐기·재발급과 코드·이력 정리 전에는 공개용 복제본을 만들지 않습니다.

## API 구성

- `/api`: 회원가입·로그인·프로필
- `/api/post`: 게시글 CRUD와 지원서 조회
- `/api/apply`: 지원서 작성·조회
- `/api/chat`: 채팅방·메시지

`applicationRoutes.js`의 `getApplicationsByPostId:postId` 경로는 매개변수 앞 구분자 확인이 필요한 후속 수정 항목입니다. README의 기대 경로를 실제 구현으로 오인하지 않도록 명시합니다.

<details>
<summary>프로젝트 화면</summary>

![TeamMate 화면](https://github.com/user-attachments/assets/a945bc70-8b75-470d-a67f-4156bb0fc974)

</details>
