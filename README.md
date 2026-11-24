# Spelling Stars ⭐ (Brown Class)

Brown Class 스펠링 시험 연습 앱이에요. 단어를 듣고 배운 뒤, 발음을 듣고 화면 키보드로 철자를 맞히는 퀴즈를 풀어요.
GitHub Pages로 배포하는 PWA라서, 태블릿에서 한 번 열고 홈 화면에 추가하면 그다음부터는 인터넷 없이 실행돼요.

## 태블릿에 설치하기 (안드로이드)

1. 태블릿의 **Chrome**에서 GitHub Pages 주소(`https://<아이디>.github.io/spelling-stars/`)를 엽니다.
2. 오른쪽 위 **⋮ → 홈 화면에 추가**(또는 "앱 설치")를 누릅니다.
3. 홈 화면의 ⭐ **Spelling Stars** 아이콘으로 실행하면 전체 화면 앱으로 열려요.
4. 처음 한 번 연 뒤에는 Wi-Fi가 꺼져 있어도 동작해요.

**발음이 안 나올 때:** 설정 → 일반 → 텍스트 음성 변환에서 Google 음성 서비스를 선택하고, **English (United States)** 음성 데이터를 내려받아 두세요.

## 단어 바꾸기

1. `index.html`의 `const SETS=[ ... ]` 부분을 수정합니다. (GitHub 웹에서 ✏️ 버튼으로 바로 고칠 수 있어요.)
   ```js
   ["12/1","Tue",["rice","mice","twice","price","spice"]],
   ```
2. `sw.js`의 `const VERSION = "v1";` 숫자를 하나 올립니다(v2, v3…). 이 숫자를 올려야 태블릿이 새 단어를 받아요.
3. 태블릿에서 인터넷이 연결된 상태로 앱을 한 번 열었다가 닫고 다시 열면 새 단어가 보여요.

## 파일 구성

- `index.html`: 앱 전체(화면, 단어, 퀴즈)
- `sw.js`: 오프라인 캐시
- `manifest.webmanifest`, `icons/`: 홈 화면 아이콘과 앱 정보
- `fonts/`: DM Sans, Comic Relief (SIL Open Font License)
