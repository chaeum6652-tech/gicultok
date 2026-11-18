# 기출톡 - 사회복지사 1급 1교시

업로드된 2026년도 제24회 사회복지사 1급 1교시 A형 문제지의 50문항을 담은 Android Studio 프로젝트입니다.

## 기능
- 50문항 객관식 퀴즈 (전체/과목별)
- 보기 선택, 이전/다음, 문제 번호 이동
- 공식 정답 50개 반영 및 정답 수정
- 채점, 정답률, 오답노트, 오답 재응시
- 로컬 기기 저장 및 학습기록 JSON 백업/복원

## APK 빌드 방법 A: GitHub Actions (클라우드 빌드)
1. 이 프로젝트 압축을 풀고 GitHub에 새 저장소를 만듭니다.
2. 프로젝트 파일 전체를 저장소에 업로드합니다. (`.github/workflows/android-apk.yml` 포함)
3. GitHub 저장소의 **Actions → Build Android APK → Run workflow**를 실행합니다.
4. 작업이 끝나면 실행 결과 하단 **Artifacts**에서 `gichultok-debug-apk`를 다운로드합니다.
5. ZIP 압축을 풀면 `app-debug.apk`가 있습니다. Android 휴대폰으로 옮겨 설치하세요.

## APK 빌드 방법 B: Android Studio (PC 빌드)
1. Android Studio에서 이 폴더를 엽니다.
2. JDK 17, Android SDK Platform 35, Build Tools 35.0.0을 설치합니다.
3. Gradle 8.9로 프로젝트를 동기화합니다.
4. **Build → Build Bundle(s) / APK(s) → Build APK(s)**를 선택합니다.
5. APK 경로: `app/build/outputs/apk/debug/app-debug.apk`

## 정답 데이터
정답은 사용자가 대화에 첨부한 공식 정답표 이미지의 1~50번을 직접 반영했습니다. 앱의 정답 수정 메뉴에서 변경할 수 있습니다.

## 데이터 출처 및 확인사항
문제와 보기는 사용자가 올린 PDF에서 추출했습니다. OCR/텍스트 추출 오류가 있을 수 있으므로 문제 문구는 원본 PDF와 대조해 주세요.

## 참고
현재 프로젝트는 Android WebView 기반의 로컬 앱입니다. 네트워크 연결 없이 문제 풀이와 기록 저장이 가능하도록 구성했습니다. GitHub Actions 워크플로는 APK를 빌드해 다운로드 가능한 artifact로 제공합니다.
