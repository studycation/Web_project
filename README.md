# Web_project
웹 제작 프로젝트

# FE 구조
├── FE
│   ├── public
│   │   ├── favicon.ico
│   │   ├── images
│   │   ├── index.html
│   │   └── vite.svg
│   └── src
│       ├── App.css
│       ├── App.tsx
│       ├── assets
│       │   ├── fonts
│       │   ├── icons
│       │   └── react.svg
│       ├── components
│       │   ├── auth
│       │   │   ├── LoginModal.tsx
│       │   │   └── SignupForm.tsx
│       │   ├── common
│       │   │   ├── Button.tsx
│       │   │   ├── LoadingSpinner.tsx
│       │   │   └── Modal.tsx
│       │   ├── error
│       │   │   └── ErrorBoundary.tsx
│       │   ├── game
│       │   │   ├── GameCard.tsx
│       │   │   ├── GameFilterBar.tsx
│       │   │   ├── GameLikeButton.tsx
│       │   │   ├── GameList.tsx
│       │   │   ├── GamePlayet.tsx
│       │   │   ├── GameSearchBar.tsx
│       │   │   ├── GameSortSelector.tsx
│       │   │   └── GameUploadForm.tsx
│       │   ├── layout
│       │   │   ├── Footer.tsx
│       │   │   └── Header.tsx
│       │   ├── mypage
│       │   │   ├── creator
│       │   │   ├── guestbook
│       │   │   ├── MyNavigation.tsx
│       │   │   ├── MyProfile.tsx
│       │   │   ├── myroom
│       │   │   └── post
│       │   └── review
│       │       ├── ReviewForm.tsx
│       │       ├── ReviewItem.tsx
│       │       └── ReviewList.tsx
│       ├── config
│       │   ├── appConstants.ts
│       │   ├── firebaseConfig.ts
│       │   ├── routes.tsx
│       │   └── theme.ts
│       ├── hooks
│       │   ├── useAuth.ts
│       │   ├── useCreator.ts
│       │   ├── useGameSearch.ts
│       │   ├── useGame.ts
│       │   ├── useGuestbook.ts
│       │   ├── useLikeGame.ts
│       │   ├── useMyroom.ts
│       │   └── usePost.ts
│       ├── index.css
│       ├── main.tsx
│       ├── pages
│       │   ├── GameDetailPage.tsx
│       │   ├── GameListPage.tsx
│       │   ├── GameUploadPage.tsx
│       │   ├── Home.tsx
│       │   ├── LoginPage.tsx
│       │   ├── MyPage
│       │   │   ├── CreatorHomePage.tsx
│       │   │   ├── GuestBookPage.tsx
│       │   │   ├── index.tsx
│       │   │   ├── MyRoomPage.tsx
│       │   │   └── PostPage.tsx
│       │   └── NotFoundPage.tsx
│       ├── query
│       │   ├── gameQuery.ts
│       │   ├── guestbookQuery.ts
│       │   ├── myroomQuery.ts
│       │   ├── postQuery.ts
│       │   ├── queryClient.ts
│       │   ├── reviewQuery.ts
│       │   └── userQuery.ts
│       ├── service
│       │   ├── firebaseService.ts
│       │   ├── gameService.ts
│       │   ├── reviewService.ts
│       │   └── userService.ts
│       ├── stores
│       │   ├── authStore.ts
│       │   ├── creatorStore.ts
│       │   ├── gameStore.ts
│       │   ├── guestbookStore.ts
│       │   ├── myroomStore.ts
│       │   └── postStore.ts
│       ├── styles
│       │   ├── globals.css
│       │   └── tailwind.css
│       ├── types
│       │   ├── game.ts
│       │   ├── guestbook.ts
│       │   ├── myroom.ts
│       │   ├── post.ts
│       │   ├── review.ts
│       │   └── user.ts
│       └── vite-env.d.ts
├── GEMINI.md
├── index.html
├── package.json
├── package-lock.json
├── README.md
├── tailwind.config.js
├── tsconfig.app.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
