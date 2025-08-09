# Web_project
웹 제작 프로젝트

# FE 구조
```
frontend/                                 # 프론트엔드 관련 파일들
├── node_modules/                         # 프로젝트 종속성 모듈
├── public/                               # 정적 파일들
│   ├── images/                           # 이미지 파일들
│   ├── favicon.ico                       # 파비콘 파일
│   └── index.html                        # 메인 HTML 파일
├── src/                                  # 소스 코드
│   ├── assets/                           # 정적 자산 파일들
│   │   ├── fonts/                        # 폰트 파일들
│   │   └── icons/                        # 아이콘 파일들
│   ├── components/                       # 재사용 가능한 UI 컴포넌트(위젯)
│   │   ├── common/                       # 공통 UI(버튼, 모달, 로딩 스피너 등)
│   │   │   ├── Button.tsx                # 범용 버튼 컴포넌트
│   │   │   ├── Modal.tsx                 # 범용 모달 컴포넌트
│   │   │   ├── LoadingSpinner.tsx        # 로딩 스피너 컴포넌트
│   │   │   └── ...                      # 기타 공통 컴포넌트
│   │   ├── layout/                       # 레이아웃 컴포넌트(Header, Footer)
│   │   │   ├── Header.tsx                # 헤더 컴포넌트
│   │   │   └── Footer.tsx                # 푸터 컴포넌트
│   │   ├── auth/                         # 인증 관련 컴포넌트
│   │   │   ├── LoginModal.tsx            # 로그인 모달 컴포넌트
│   │   │   └── SignupForm.tsx            # 회원가입 폼 컴포넌트
│   │   ├── game/                         # 게임 관련 UI 컴포넌트
│   │   │   ├── GameCard.tsx              # 게임 카드 컴포넌트
│   │   │   ├── GameList.tsx              # 게임 목록 렌더링 컴포넌트
│   │   │   ├── GameSearchBar.tsx         # 게임 검색 바 컴포넌트
│   │   │   ├── GameFilterBar.tsx         # 주제(카테고리)/정렬 필터 바 컴포넌트
│   │   │   ├── GameSortSelector.tsx      # 인기순 등 정렬 선택 컴포넌트
│   │   │   ├── GameLikeButton.tsx        # 게임 상세 내 좋아요 버튼 컴포넌트
│   │   │   ├── GamePlayer.tsx            # 게임 실행(iframe/WebGL) 컴포넌트
│   │   │   └── GameUploadForm.tsx        # 게임 업로드 폼 컴포넌트
│   │   ├── review/                       # 댓글/리뷰 UI 컴포넌트 (게임 상세 포함)
│   │   │   ├── ReviewList.tsx            # 댓글 목록 컴포넌트
│   │   │   ├── ReviewForm.tsx            # 댓글 작성 폼 컴포넌트
│   │   │   └── ReviewItem.tsx            # 개별 댓글 아이템 컴포넌트
│   │   ├── mypage/                       # 마이페이지 관련 컴포넌트
│   │   │   ├── MyProfile.tsx             # 사용자 프로필 컴포넌트
│   │   │   ├── MyNavigation.tsx          # 마이페이지 내 네비게이션 탭/메뉴 컴포넌트
│   │   │   ├── creator/                  # 창작자 관련 컴포넌트 하위 폴더
│   │   │   │   ├── CreatorProfile.tsx    # 창작자 프로필/소개 컴포넌트
│   │   │   │   ├── CreatorGames.tsx      # 창작자 게임 목록 컴포넌트
│   │   │   │   ├── CreatorPostList.tsx   # 창작자 게시글(공지사항 등) 목록 컴포넌트
│   │   │   │   ├── CreatorPostDetail.tsx # 창작자 게시글 상세 페이지 컴포넌트
│   │   │   │   └── CreatorPostEditor.tsx # 창작자 게시글 작성/수정 페이지 컴포넌트
│   │   │   ├── post/                     # 게시글 관련 컴포넌트 하위 폴더
│   │   │   │   ├── PostList.tsx          # 게시글 목록 컴포넌트
│   │   │   │   ├── PostDetail.tsx        # 게시글 상세 페이지 컴포넌트
│   │   │   │   └── PostEditor.tsx        # 게시글 작성/수정 페이지 컴포넌트
│   │   │   ├── guestbook/                # 방명록 관련 컴포넌트 하위 폴더
│   │   │   │   ├── GuestbookList.tsx     # 방명록 리스트 컴포넌트
│   │   │   │   ├── GuestbookForm.tsx     # 방명록 작성 폼 컴포넌트
│   │   │   │   └── GuestbookItem.tsx     # 방명록 카드 아이템 컴포넌트
│   │   │   └── myroom/                   # 마이룸 관련 컴포넌트 하위 폴더
│   │   │       ├── MyRoomView.tsx        # 마이룸 메인 뷰 컴포넌트
│   │   │       ├── MyRoomEditor.tsx      # 마이룸(꾸미기 등) 에디터 컴포넌트
│   │   │       └── MyRoomItem.tsx        # 마이룸 아이템/소품 컴포넌트 예시
│   │   └── error/                        # 에러 처리 관련 컴포넌트
│   │       └── ErrorBoundary.tsx         # 에러 경계 컴포넌트
│   ├── config/                           # 설정 파일들 폴더
│   │   ├── firebaseConfig.ts             # Firebase 설정 파일
│   │   ├── routes.tsx                    # 라우트 정의 파일
│   │   ├── appConstants.ts               # 전역 상수 정의 파일
│   │   └── theme.ts                      # 테마 및 디자인 시스템 설정 파일
│   ├── query/                            # TanStack Query 관련(fetch/mutation) 파일 모음
│   │   ├── gameQuery.ts                  # 게임 목록, 상세, 검색, 정렬, 좋아요 관련 쿼리
│   │   ├── reviewQuery.ts                # 댓글/리뷰 관련 쿼리
│   │   ├── userQuery.ts                  # 유저 및 창작자 정보 관련 쿼리
│   │   ├── postQuery.ts                  # 게시글 관련 쿼리
│   │   ├── myroomQuery.ts                # 마이룸 관련 쿼리
│   │   ├── guestbookQuery.ts             # 방명록 관련 쿼리
│   │   └── queryClient.ts                # QueryClient 인스턴스 및 설정 (Provider 포함)
│   ├── stores/                           # zustand 상태관리 store(전역 UI 상태 등)
│   │   ├── authStore.ts                  # 인증 및 유저 상태 관리 store
│   │   ├── gameStore.ts                  # 게임 목록/상세 UI 상태 store
│   │   ├── creatorStore.ts               # 창작자 및 커스터마이징 상태 store
│   │   ├── postStore.ts                  # 게시글 상태 관리 store
│   │   ├── myroomStore.ts                # 마이룸 상태관리 store
│   │   └── guestbookStore.ts             # 방명록 상태관리 store
│   ├── hooks/                            # 커스텀 훅 모음
│   │   ├── useAuth.ts                    # 인증 관련 훅
│   │   ├── useGame.ts                    # 게임 관련 훅
│   │   ├── useGameSearch.ts              # 게임 검색/필터 훅
│   │   ├── useLikeGame.ts                # 좋아요 토글 훅 (TanStack Query mutation 래핑)
│   │   ├── useCreator.ts                 # 창작자 관련 훅
│   │   ├── usePost.ts                    # 게시글 훅
│   │   ├── useMyroom.ts                  # 마이룸 훅
│   │   └── useGuestbook.ts               # 방명록 훅
│   ├── pages/                           # 페이지 컴포넌트들(라우트 단위)
│   │   ├── Home.tsx                      # 홈(메인) 페이지
│   │   ├── GameListPage.tsx              # 게임 목록 페이지 (검색, 필터, 정렬 포함)
│   │   ├── GameDetailPage.tsx            # 게임 상세 페이지 (좋아요, 댓글 포함)
│   │   ├── GameUploadPage.tsx            # 게임 업로드 페이지
│   │   ├── MyPage/                       # 마이페이지 및 하위 라우트 폴더
│   │   │   ├── index.tsx                 # 마이페이지 메인(내 활동 및 프로필)
│   │   │   ├── CreatorHomePage.tsx       # 작가홈 페이지
│   │   │   ├── PostPage.tsx              # 게시글 페이지(나의 게시글)
│   │   │   ├── GuestbookPage.tsx         # 방명록 페이지
│   │   │   └── MyRoomPage.tsx             # 마이룸 페이지 (다이어리 → 마이룸 반영)
│   │   ├── LoginPage.tsx                 # 로그인 및 회원가입 페이지
│   │   └── NotFoundPage.tsx              # 404 Not Found 페이지
│   ├── service/                          # API 통신 및 서비스 모듈
│   │   ├── firebaseService.ts            # Firebase 관련 API 서비스
│   │   ├── gameService.ts                # 게임 관련 API 서비스
│   │   ├── reviewService.ts              # 리뷰/댓글 관련 API 서비스
│   │   └── userService.ts                # 유저 정보 관련 API 서비스
│   ├── styles/                          # 스타일 관련 파일들
│   │   ├── globals.css                   # 전역 스타일
│   │   └── tailwind.css                  # Tailwind CSS 설정 파일
│   ├── types/                           # 타입 정의 파일들
│   │   ├── game.ts                       # 게임 관련 타입 정의
│   │   ├── user.ts                       # 유저 및 창작자 타입 정의
│   │   ├── review.ts                     # 리뷰 및 댓글 타입 정의
│   │   ├── post.ts                       # 게시글 타입 정의
│   │   ├── myroom.ts                     # 마이룸 타입 정의
│   │   └── guestbook.ts                  # 방명록 타입 정의
│   ├── App.tsx                          # 앱 메인 컴포넌트
│   ├── App.css                          # 앱 전체 스타일 파일
│   ├── index.tsx                        # 앱 렌더링 진입점
│   └── index.css                        # 인덱스 페이지 스타일 파일
├── .env                                # 환경 변수 파일
├── package-lock.json                   # 패키지 버전 잠금 파일
├── package.json                        # 프로젝트 설정 및 종속성 정의 파일
├── tailwind.config.js                  # Tailwind CSS 설정 파일
└── tsconfig.json              
```
