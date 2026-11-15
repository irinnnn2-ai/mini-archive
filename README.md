# mini-archive

미니 님의 개인 스크랩 아카이브입니다. 노무사 시험·부동산·개원 플랜·자산관리처럼 계속 챙겨야 하는 것들을 한 페이지에 모아 두고, 하루 한 번 아침 브리핑을 함께 봅니다.

- 페이지: **https://irinnnn2-ai.github.io/mini-archive/**
- `index.html` — 아카이브 본체 (단일 파일, 인라인 CSS/JS). 모바일 우선 반응형, 검색엔진 노출 차단(`noindex, nofollow`).
- `robots.txt` — 검색엔진 수집 차단(`Disallow: /`).

## ⚠️ 배포는 `gh-pages` 브랜치에서 이뤄집니다

GitHub Pages가 `gh-pages` 브랜치의 루트(`/`)를 바라보고 있습니다(`build_type: legacy`). Pickle의 GitHub 연결 토큰에는 Pages 설정을 바꿀 권한이 없어서, `gh-pages` 브랜치를 푸시했을 때 GitHub가 자동으로 만든 설정 그대로입니다.

- `index.html`을 고칠 때는 **`main`과 `gh-pages` 양쪽에** 반영해야 사이트에 보입니다.
- 이 저장소를 클론했다면 아래 한 줄로 두 브랜치를 함께 올릴 수 있습니다:
  `git push origin main:main main:gh-pages`
- GitHub 저장소 → Settings → Pages → Source를 `main` / `(root)`로 바꾸면 `gh-pages` 없이 `main`만으로 배포됩니다. (선택 사항)

## 매일 아침 브리핑 교체

`index.html`에서 아래 두 주석 **사이의 내용만** 바꾸고 커밋하면 됩니다. 나머지 화면은 그대로 유지됩니다.

```html
<!-- MORNING_BRIEFING_START -->
<div class="briefing-body" id="morningBriefing">
  ... (이 부분만 교체)
</div>
<!-- MORNING_BRIEFING_END -->
```

`<p>`, `<ul>`, `<strong>`, `<a>` 정도의 태그를 쓰면 카드 안에서 자연스럽게 보입니다.

## 기록은 어디에 저장되나요

항목은 서버가 아니라 **각 기기 브라우저의 localStorage**에 저장됩니다. 휴대폰과 PC의 목록은 서로 별개이니, 기기를 바꾸거나 옮길 때는 페이지 하단의 `JSON 내보내기`로 파일을 받아 새 기기에서 `JSON 불러오기`로 복원하세요.

## 화면

`preview.png` — 모바일(412×915) 미리보기 스크린샷. 저장소에는 올리지 않습니다(`.gitignore`).
