Paper Immersive v2 — iPad PDF 뷰어

기능
- PDF 직접 등록, 최근 파일 다시 열기, 등록한 파일 선택/삭제, PDF 원본 저장/공유.
- 앱 시작 시 PDF가 없으면 등록 화면, 문서 로딩 후에는 메뉴 완전히 숨김.
- PDF 한 번 탭: 아무 동작 없음 / 두 번 탭: 도구 막대 토글.
- 두 손가락 핀치: 10%~400% 확대·축소 (화면 너비에 맞춘 100% 기준).
- 축소한 PDF가 화면보다 작아지면 흰 바탕의 중앙에 배치. 세로 스크롤이 필요한 문서는 위아래로만 이동.
- 도구 막대를 켜면 [-] [확대율 100%] [슬라이더] [+] (100% 누르면 너비 맞춤).
- PDF.js는 최초 온라인 접속에 필요. 파일 데이터는 서버에 전송하지 않고 기기 로컬 IndexedDB에 저장.

GitHub Pages 업데이트
1. ZIP을 풀고 안의 index.html, app.js, manifest.json, sw.js, icon-192.png, icon-512.png를
   기존 GitHub Pages 저장소의 최상위 파일과 각각 교체합니다. README_설치.txt는 선택 사항.
2. GitHub의 Settings > Pages: Deploy from a branch / main / (root)로 설정합니다.
3. 배포가 끝나면 Safari 및 홈화면 웹앱에서 새로고침(이전 버전 캐시가 남으면 앱을 완전히 닫고 다시 열기)합니다.
4. 홈 화면 추가: Safari에서 배포된 HTTPS 주소 열기 > 공유 > 홈 화면에 추가 > 웹 앱으로 열기 켜기.

중요한 iPadOS 제한
- iPad 홈 화면 웹앱(PWA)은 Safari 주소창과 하단 브라우저 메뉴를 제거할 수 있습니다.
- 그러나 iPadOS가 표시하는 시각/배터리/상단 상태 표시줄은 PWA에서 반드시 숨길 수 있는 대상이 아닙니다.
  manifest의 display:fullscreen 및 apple-mobile-web-app-status-bar-style:black-translucent조차
  iPadOS 버전에 따라 시스템 상태 표시줄을 유지합니다.
- 시각·배터리까지 강제로 숨기는 기능은 이 웹앱에 포함되지 않습니다.
  이 버전에는 네이티브 앱이 포함되어 있지 않습니다. 상태 표시줄 숨김은 지원하지 않습니다.
- 홈 인디케이터/시스템 제스처는 네이티브 앱에서도 OS가 일시적으로 표시할 수 있습니다.

단일 HTML 시험용
- 별도 제공하는 Paper_iPad_몰입형_v2_시험용.html은 HTML 하나에 앱 내용을 포함하며,
  서버에서 열어 시험하기 편합니다. Files 앱의 HTML 미리보기에서는 PDF.js 모듈이 제한될 수 있습니다.
- 일반 Safari 탭에서 열면 Safari 주소창 및 시스템 상태바는 앱이 감출 수 없습니다.

주의: 실제 iPad에서 직접 동작 확인은 할 수 없었고, 웹 동작은 Chromium 모바일 모의환경에서 점검했습니다.
