# RealSnap Mobile — Prototype

RealSnap 웹앱 리뉴얼의 **모바일 화면 프로토타입**이에요. 화면 15개가 HTML 파일 하나에 들어 있고, 클릭해서 화면 사이를 이동할 수 있어요.

## 실행

폰트와 영상을 `assets/`에서 불러오기 때문에, 파일을 더블클릭하지 말고 **로컬 서버**나 **GitHub Pages**로 열어야 해요.

```bash
# 로컬
python3 -m http.server 8000
# → http://localhost:8000
```

**GitHub Pages:** Settings → Pages → Branch `main` / `root`로 설정하면 `https://<user>.github.io/<repo>/`에서 열려요.

- 크롬 개발자도구에서 모바일 뷰(390 × 844)로 보는 걸 권장해요.
- 데스크탑 화면에서는 390px 폭으로 가운데에 표시돼요.
- 왼쪽 하단 **Screens** 버튼을 누르면 화면 목록이 열려요. 이 버튼은 프로토타입 탐색용이라 실제 UI에는 들어가지 않아요.
- 특정 화면으로 바로 가려면 URL 해시를 쓰면 돼요. 예: `#MobilePricing`

## 화면 목록

| 해시 | 화면 |
|---|---|
| `#MobileTry` | 홈 (비로그인) — 무료 크레딧 / 무드 캔버스 배너, 툴 선택, Contact sales 버튼 |
| `#MobileHomeSigned` | 홈 (로그인) — 크레딧 칩 |
| `#MobileMenu` | 햄버거 메뉴 — 친구 초대, Editorial / Updates / Pricing, 언어 |
| `#MobileTool` | 툴 화면 (기본) |
| `#MobileVarBLookbook` | 툴 — Lookbook |
| `#MobileVarBStudio` | 툴 — Studio Shot |
| `#MobileVarBProduct` | 툴 — Product Shot |
| `#MobileSetup` | 스타일 선택 시트 |
| `#MobilePhoto` | 사진 추가 시트 |
| `#MobileLimit` | 생성 시 가입 유도 시트 |
| `#MobileResult` | 결과 (생성 중 → 완료) |
| `#MobileStyle` | 스타일 풀스크린 뷰어 |
| `#MobileNoCredits` | 크레딧 부족 — 요금제 / 친구 초대 |
| `#MobilePricing` | 요금제 (월간 / 연간, Enterprise) |
| `#MobileContact` | 데모 신청 폼 (20 크레딧) |

## 주요 정책 (프로토타입 기준)

- 가입 시 무료 **5 크레딧**
- 친구 초대: 친구가 가입하면 초대한 사람에게 **20 크레딧**
- 온라인 데모 신청: **20 크레딧**
- 크레딧 소모: Lookbook 1.5, Studio Shot 1, Product Shot 1
- 요금제: Freelancer $49 (연간 $44), Agency $298 (연간 $268), Enterprise 별도 문의

## 파일 구성

```
index.html                     모든 화면 + 런타임 (React 18.3.1 포함, 외부 요청 없음)
assets/
  PretendardJPVariable.woff2   폰트
  film-lookbook2.mp4           툴 화면 필름 스트립 — Lookbook
  film-studio.mp4              툴 화면 필름 스트립 — Studio Shot
  film-product2.mp4            툴 화면 필름 스트립 — Product Shot
  mc-mobile4.mp4               홈 배너 — Mood Canvas
```

## 디자인 토큰

| 용도 | 값 |
|---|---|
| 브랜드 레드 | `#e8251a` |
| 텍스트 / 프라이머리 버튼 | `#09090b` |
| 보조 텍스트 | `#71717a` |
| 보더 | `#e4e4e7` |
| 서피스 | `#fafafa` / `#f4f4f5` |
| 폰트 | Pretendard JP Variable |
| 버튼 높이 / 라운드 | 48px / 10px |
| 사이드 여백 | 16px |

## 참고

- 디자인 확인용 프로토타입이라 실제 로그인, 결제, 생성 기능은 없고 상태만 흉내 내요.
- 이미지는 데모용 샘플이에요.
- Pretendard JP는 SIL Open Font License 1.1을 따라요.
