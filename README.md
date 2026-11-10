# 트럼펫 운지 퀴즈 — GitHub Pages 배포판

B♭ 트럼펫의 기보음과 운지를 연습하는 정적 웹사이트입니다. 빌드 도구, 서버, 데이터베이스가 필요하지 않습니다.

## 파일 구성

- `index.html`: 사이트 화면과 퀴즈 로직
- `assets/vexflow-5.0.0.js`: 로컬 고정된 VexFlow 악보 렌더러
- `assets/VEXFLOW-LICENSE.txt`: VexFlow MIT 라이선스
- `.nojekyll`: GitHub Pages의 Jekyll 처리를 비활성화

모든 브라우저 경로는 상대경로이므로 아래 두 방식에서 모두 동작합니다.

- 사용자 사이트: `https://GITHUB_ID.github.io/`
- 프로젝트 사이트: `https://GITHUB_ID.github.io/REPOSITORY/`

## 방법 1: 사용자 사이트로 배포

GitHub에서 공개 저장소를 만들고 저장소 이름을 정확히 `GITHUB_ID.github.io`로 지정합니다. 이 폴더 안의 파일을 저장소 최상위에 업로드합니다.

터미널을 사용한다면 이 폴더에서 다음 명령을 실행합니다.

```bash
git init
git add .
git commit -m "Publish trumpet fingering quiz"
git branch -M main
git remote add origin https://github.com/GITHUB_ID/GITHUB_ID.github.io.git
git push -u origin main
```

그다음 저장소의 **Settings → Pages → Build and deployment**에서 다음을 선택합니다.

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/(root)`

주소는 `https://GITHUB_ID.github.io/`입니다.

## 방법 2: 프로젝트 사이트로 배포

저장소 이름은 자유롭게 지정할 수 있습니다. 예를 들어 `trumpet-fingering`으로 만들고 이 폴더 안의 파일을 저장소 최상위에 업로드합니다.

Pages 설정은 사용자 사이트와 동일합니다.

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/(root)`

주소는 `https://GITHUB_ID.github.io/trumpet-fingering/`입니다.

## 무료 플랜 주의사항

GitHub Free에서 Pages를 사용하려면 저장소가 공개 상태여야 합니다. 사이트에 개인정보나 비밀값을 넣지 마세요. 현재 배포판에는 사용자 데이터나 비밀값이 없습니다.
