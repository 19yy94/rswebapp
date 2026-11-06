# RealSnap Web App — Renewal Prototype (B안)

RealSnap 웹앱 리뉴얼의 **데스크탑 + 모바일 화면 프로토타입**이에요. 화면 44개가 `index.html` 하나에 들어 있고, 클릭해서 화면 사이를 이동할 수 있어요.

## 실행

`index.html` 하나에 폰트, 이미지, 영상, 런타임(React 18.3.1)이 모두 들어 있어서 외부 요청이 없어요.

- 더블클릭으로 바로 열 수 있어요.
- 로컬 서버(`python3 -m http.server 8000`)나 **GitHub Pages**(Settings → Pages → `main` / `root`)로 열어도 돼요.
- 파일 크기는 약 21MB예요. 영상과 이미지가 파일 안에 들어 있어서 그래요.

## 둘러보기

- 왼쪽 하단 **Screens** 버튼을 누르면 전체 화면 목록이 열려요. 이 버튼은 프로토타입 탐색용이라 실제 UI에는 들어가지 않아요.
- 특정 화면으로 바로 가려면 URL 해시를 쓰면 돼요. 예: `index.html#Create`, `index.html#MobileTry`
- 데스크탑 화면은 1440px 기준이에요.
  - 1023px 이하(iPad 세로)에선 사이드바가 아이콘만 남기고 자동으로 접혀요.
  - 홈과 Create 배너는 1360px을 기준으로 와이드 이미지와 중간 폭 이미지가 바뀌어요.
- 모바일 화면(`Mobile…`)은 390px 폭으로 가운데에 표시돼요.

## 화면 목록

### 데스크탑 — 홈

| 해시 | 화면 |
|---|---|
| `#Main` | 홈 (로그인) — 무드 캔버스 배너, 퀵스타트 |
| `#MainNew` | 홈 (첫 로그인) — 5 크레딧 웰컴 배너, 시작 가이드 |
| `#HomeGuest` | 홈 (비로그인) — 무료 크레딧 / 무드 캔버스 롤링 배너, 툴 썸네일 |
| `#SignupGate` | 생성 시 가입 유도 |

### 데스크탑 — 만들기

| 해시 | 화면 |
|---|---|
| `#Create` | Create — 롤링 배너, 기능 목록 (Image / Video / Design) |
| `#MoodCanvas` | Mood Canvas — 템플릿, 내 캔버스 |
| `#MoodCanvasEditor` | Mood Canvas 에디터 (노드) |
| `#Lookbook` 외 `#Lookbook…` 13개 | 룩북 — 빈 화면, 생성 중, 결과, 스타일·모델·포즈·카메라 설정, Correct, 버전 비교, 10장 배치 |
| `#EditImage` | Retouch |
| `#FashionFilm` | Fashion Film |
| `#ProductShot` | Product Shot |

### 데스크탑 — 탐색 · 계정

| 해시 | 화면 |
|---|---|
| `#Styles` | Explore — 스타일 |
| `#ExploreCanvases` | Explore — 무드 캔버스 |
| `#Assets` | Assets — 결과물, 캔버스, 업로드, 브랜드 |
| `#Pricing` | Plans & Credits — 요금제, Enterprise 모듈 |
| `#ContactSales` | Contact sales 폼 |
| `#Help` | Tutorials & Help |
| `#AccountMenu` | 계정 메뉴 열림 (크레딧, 친구 초대, 언어) |
| `#CreditLevels` | 크레딧 링 단계별 표시 |

### 모바일

| 해시 | 화면 |
|---|---|
| `#MobileTry` | 홈 (비로그인) — 배너, 툴 선택, Contact sales 버튼 |
| `#MobileHomeSigned` | 홈 (로그인) — 크레딧 칩 |
| `#MobileMenu` | 햄버거 메뉴 — 친구 초대, Editorial / Updates / Pricing, 언어 |
| `#MobileTool` | 툴 화면 |
| `#MobileSetup` | 스타일 선택 시트 |
| `#MobilePhoto` | 사진 추가 시트 |
| `#MobileLimit` | 생성 시 가입 유도 시트 |
| `#MobileResult` | 결과 (생성 중 → 완료) |
| `#MobileStyle` | 스타일 풀스크린 뷰어 |
| `#MobileNoCredits` | 크레딧 부족 — 요금제 / 친구 초대 |
| `#MobilePricing` | 요금제 |
| `#MobileContact` | Contact sales 폼 |

## 주요 정책 (프로토타입 기준)

- 가입 시 무료 **5 크레딧**
- 친구 초대: 친구가 가입하면 초대한 사람에게 **20 크레딧**
- 크레딧 소모: Lookbook 1.5, Studio Shot 1, Product Shot 1
- 요금제
  - Freelancer: 월 $49 (연간 결제 시 $44)
  - Agency: 월 $298 (연간 결제 시 $268)
  - Enterprise: 별도 문의 → Contact sales 폼으로 연결
- 툴: Lookbook, Studio Shot, Product Shot, Acc Lookbook, Multi Shot, Location, Retouch, Fashion Film, Video Editor, Mood Canvas, Campaign Graphics, Design Studio
  - Video Editor와 Design Studio는 Enterprise 전용이에요.
- 라이트 모드만 있어요. 다크 모드는 뺐어요.

## 디자인 토큰

| 용도 | 값 |
|---|---|
| 브랜드 레드 | `#e8251a` |
| 텍스트 / 프라이머리 버튼 | `#09090b` / `#18181b` |
| 보조 텍스트 | `#71717a` |
| 보더 | `#e4e4e7` |
| 서피스 | `#fafafa` / `#f4f4f5` |
| 폰트 | Pretendard JP Variable (본문), Druk Wide Medium (캠페인 헤드라인) |
| UI 라이브러리 기준 | shadcn/ui |

## 참고

- 디자인 확인용 프로토타입이라 실제 로그인, 결제, 생성 기능은 없고 상태만 흉내 내요.
- 이미지와 영상은 데모용 샘플이에요.
- Pretendard JP는 SIL Open Font License 1.1을 따라요.
