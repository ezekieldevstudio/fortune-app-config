# FO PICK public configuration repository

## 최신 관리 현황 — 2026-10-26

- 앱: FO PICK / com.ezekiel.fopick / 앱 프로젝트: fortune-app
- 로컬 경로: C:\dev\EzekielDev\fortune-app-config
- 앱 단계: 프로덕션 액세스 승인 확인 / 1.0.1 출시 준비·신규 기능 동결
- Play: 1.0.0 / code 1 · 비공개 Alpha 마지막 확인. 1.0.1 / code 2 프로덕션 제출 완료 근거 없음
- 소스/native: 1.0.1 / 2 (세부 불일치·목표는 앱 README 참고)

### 공개 파일과 운영

faq.json, faq-locales.v1.json, notices.json, privacy-policy.html

로컬 12개 언어 FAQ·영문 정책 존재. 최신 공개 게시 상태 미확인. 공개 정적 파일용 저장소이며 앱 package/versionCode와 별도의 콘텐츠 형식을 유지한다. Secret·서명 파일·사용자 기록을 넣지 않는다.

### 현재 문제 / 다음 작업

2026-10-26 Play Console에서 프로덕션 액세스 승인 확인. 개인정보처리방침에 운영 연락처 ezekieldevstudio@gmail.com을 반영하고 개발 중 임시 안내를 정리했다. 공개 URL 반영 확인은 별도 수행한다. FAQ/공지 JSON과 광고·저장 정책의 의미는 변경하지 않았다.

### 개발 및 변경 이력 — 최신 날짜순

2026-10-26 프로덕션 출시 준비: 개인정보처리방침의 개발자 연락처와 최종 갱신일 보완. Play Alpha 1.0.0/code 1, 출시 후보 1.0.1/code 2를 구분한다. 심사 제출·게시 완료는 아직 선언하지 않는다.

2026-10-15 사용자 제출/심사 상태와 앱 README 동기화. 공개 JSON·정책 내용 및 배포 상태는 새로 검증하지 않았다.

2026-10-14 정책 연락처 미완료·앱 콘텐츠 v1 동결 상태 문서 대조. 2026-10-08 bfe541c Git 기록; 실제 게시일은 미확인.

기존 JSON·정책 본문은 이번에 수정하지 않았다. 로컬 Git만으로 원격 게시 완료를 선언하지 않는다. [앱 최신 README](../fortune-app/README.md)에서 빌드·테스트·실기기 상태와 다음 작업을 함께 관리한다.

## 기존 운영 안내 및 작성 당시 기록

이하 게시 전/미구현 표현은 작성 당시 기록이다. 현재 상태는 상단을 우선한다.

Public files for FO PICK / 포픽:

The final user-facing brand is **FO PICK / 포픽**. Repository names `fortune-app` and `fortune-app-config` and the existing public URLs remain unchanged.

- `faq.json` — Current Korean FAQ in the existing array format. All five original public IDs remain available, including `data-storage`.
- `faq-locales.v1.json` — Versioned FAQ content for `ko`, `en`, `ja`, `es`, `pt`, `fr`, `de`, `it`, `zh-Hans`, `zh-Hant`, `id`, and `vi`. Its shape is `{ schemaVersion: 1, locales: { [locale]: [{ id, question, answer }] } }`.
- `notices.json` — Notices; the initial development notice is disabled.
- `privacy-policy.html` — English Privacy Policy, intended to be served through GitHub Pages.

The Privacy Policy reflects local reading history, deletion, usage allowances, and reward access/transaction storage. History is not synchronized to a FO PICK server or account. Remote fortune content/config is not connected.

FO PICK integrates one Google AdMob banner at the bottom of Home and optional rewarded ads for two purposes: detailed access to that saved reading and one bonus regular reading after the three free periods are used. Banners are absent from selection, reveal, results, history, settings and FAQ screens. Basic readings do not require completing a rewarded ad. Additional FO PICK readings and ordinary interstitials are not provided. The policy documents SDK data handling, banner loading/refresh and rewarded preloading after UMP permits requests, privacy options, and that topic/mood and reading content are not directly supplied as ad targeting values.

The Android production App ID and three ad units are connected and verified locally in the app's ignored environment file and Expo configuration. Development uses official Google test ads. Native-device ad delivery, AdMob/UMP console validation and publication of these policy changes remain pending. This is not a claim that production ads or an updated public page are already live.

FO PICK v1 is free with a Home banner and optional rewarded ads. Premium is deferred to a later version; payment UI, SDK integration and entitlement access have been removed from the app. The policy removes the former Billing section and retains the existing AdMob/UMP, local history, usage and reward-storage disclosures.

The FAQ reflects local history, the 06:00 usage-day boundary, three regular time slots, one ad-earned regular bonus, optional rewarded detail access and the Home banner. Historical IDs `premium`, `subscription` and `restore` remain for compatibility; their visible text does not offer payments. Only the two advertising answers per language changed in this update. The multilingual file remains additive so older clients expecting the `faq.json` array are not broken. The app reads its bundled FAQ for the selected language; neither public FAQ file is fetched by the app. No notices were enabled or invented.

FAQ sources are maintained in the sibling app's `src/locales/faq.ts`. From `fortune-app`, `node scripts/sync-faq.cjs` exports the bundled Korean FAQ and both local public files. It does not publish. `node scripts/check-locales.cjs` checks that exports match their source. Translation content still needs native-speaker review.

The Privacy Policy remains one English page at the existing URL. Its verified developer contact is still missing. These local policy/FAQ changes have not been published. Korean traditional calendar context and seasonal events remain unimplemented.

## TODO

- Completed locally 2026-10-26: developer contact added to the Privacy Policy.
- Publish the reviewed policy and verify the existing GitHub Pages `privacy-policy.html` URL. Local edits alone do not update the public page.
- Verify AdMob/UMP console configuration, native-device Home banner and both rewarded placements, and interrupted reward-storage recovery before release. Local identifier and configuration checks have passed.
