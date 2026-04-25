# 글자 놀이터 APK 빌드 프로젝트 v2

이 프로젝트는 5살 아이가 한글과 영어를 게임처럼 배울 수 있는 오프라인 학습앱입니다.
이번 버전에는 요청하신 수정 사항을 반영했습니다.

## 수정된 내용

- 카드, 그림, 단어, 정답 버튼 등 주요 버튼을 누르면 한글 또는 영어 발음이 나옵니다.
- 영어 알파벳 따라 쓰기를 숫자 버튼 클릭 방식에서 실제 손가락/마우스 드로잉 방식으로 변경했습니다.
- 한글 따라 쓰기도 같은 방식으로 회색 글자 위에 직접 선을 그리며 연습합니다.
- 오프라인 실행 가능한 PWA 구성을 포함했습니다.

## 브라우저에서 바로 확인하기

압축을 풀고 아래 파일을 더블클릭하세요.

```text
www/index.html
```

## 안드로이드에서 앱처럼 설치하기: PWA 방식

1. `www` 폴더를 웹호스팅 또는 로컬 서버에 올립니다.
2. 안드로이드 Chrome에서 `index.html` 주소를 엽니다.
3. 메뉴 `⋮` → `홈 화면에 추가` 또는 `앱 설치`를 누릅니다.

## APK로 빌드하기: Android Studio + Capacitor

준비물:

- Node.js
- Android Studio
- Android SDK

순서:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

Android Studio가 열리면:

```text
Build > Build Bundle(s) / APK(s) > Build APK(s)
```

APK 위치:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

## 참고

현재 ChatGPT 실행 환경에는 Android SDK와 Gradle 빌드 도구가 없어 APK 바이너리 자체를 직접 컴파일할 수 없습니다. 위 프로젝트는 Android Studio가 설치된 PC에서 바로 APK로 변환할 수 있도록 구성되어 있습니다.
