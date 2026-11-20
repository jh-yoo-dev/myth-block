# 신화 블록

알에서 태어나는 한국·그리스·북유럽 신화 영웅 50명을 모으는 도트 블록 퍼즐.

```
docs/      게임 웹 파일 (GitHub Pages로 배포 · 앱 안에도 그대로 들어감)
android/   안드로이드 앱 프로젝트 (Android Studio로 열기)
ios/       iOS 앱 프로젝트 (Xcode로 열기)
store/     스토어 설명문·스크린샷·그래픽 이미지
assets/    앱 아이콘·스플래시 원본
```

## 운영 정보
운영자: 도트공장장 · 개인정보 보호책임자: 유주형 · 문의: jh.yoo.dev@gmail.com (약관·방침 시행일 2026-11-20)

## 1. 웹 공개 (무료)
1. GitHub에 `myth-block` 공개 저장소를 만들고 이 폴더를 올린다.
2. 저장소 Settings → Pages → Branch: `main`, 폴더: `/docs` → Save
3. 몇 분 뒤 https://jh-yoo-dev.github.io/myth-block/ 에서 열림. 휴대폰에서 "홈 화면에 추가"하면 앱처럼 실행되고 오프라인에서도 돌아감.

## 2. 앱 빌드 (맥미니)
```bash
npm install
npx cap sync          # docs/ 를 바꿨으면 매번 실행
```

### 안드로이드 (Google Play, 등록비 25달러 1회)
1. Android Studio 설치 → `npx cap open android`
2. Build → Generate Signed Bundle → Android App Bundle → 새 키스토어 만들기 (**키스토어 파일과 비밀번호는 잃어버리면 업데이트를 못 하니 꼭 백업**)
3. Play Console → 앱 만들기 → `.aab` 업로드
4. 개인 개발자 계정은 테스터 12명이 14일 동안 비공개 테스트를 해야 프로덕션 출시 가능

### iOS (Apple Developer Program, 연 129,000원)
1. Xcode 설치 → `npx cap open ios`
2. App 타깃 → Signing & Capabilities → Team 선택 (번들 ID: `dev.jhyoo.mythblock`)
3. Product → Archive → Distribute App → App Store Connect
4. App Store Connect에서 `store/listing.md` 내용과 `store/screenshots/iphone-6.7-*.png` 입력 → 심사 제출

## 게임을 고친 뒤
`docs/index.html`을 바꾸고 → GitHub에 올리면 웹은 바로 반영, 앱은 `npx cap sync` 후 버전 올려서 다시 빌드.

## 라이선스 참고
- 영웅 디자인은 공공 영역인 신화를 바탕으로 새로 그린 것 (특정 영화·게임 디자인 참조 없음)
- 글꼴: 갈무리(Galmuri) — SIL Open Font License 1.1 (`docs/FONT-LICENSE-Galmuri.md`)
