# AI Research Portfolio

대학원 진학을 준비하며 연구 관심 분야와 프로젝트 기록을 쌓아갈 수 있는 한국어 중심 정적 웹사이트입니다. 별도 설치나 빌드 없이 GitHub Pages에 올릴 수 있습니다.

## 파일 구성

```text
research-portfolio/
├─ index.html                  메인 페이지: 7개 섹션
├─ assets/
│  ├─ style.css                반응형 디자인
│  ├─ app.js                   모바일 메뉴, 프로젝트 필터
│  ├─ favicon.svg              사이트 아이콘
│  └─ project-*.svg            직접 만든 프로젝트 추상 이미지
├─ projects/
│  ├─ sarcasm-nlp.html         반어 표현 탐지 NLP
│  ├─ ai-marketing-poc.html    AI 마케팅 의사결정 지원 PoC
│  └─ jeonju-living-lab.html   전주시 공공데이터 기반 AI 리빙랩
└─ .nojekyll                   GitHub Pages에서 정적 파일 그대로 제공
```

## GitHub Pages에 올리기

1. GitHub에서 새 저장소를 만듭니다. 개인 홈페이지 주소를 원하면 저장소 이름을 `사용자명.github.io`로, 프로젝트 주소를 원하면 원하는 저장소 이름으로 정합니다.
2. 이 **폴더 안의 파일과 폴더 전체**를 저장소의 최상위에 업로드합니다. `index.html`이 저장소 최상위에 보여야 합니다. ZIP 파일 자체를 업로드하면 사이트가 열리지 않습니다.
3. 변경 사항을 `main` 브랜치에 커밋합니다.
4. 저장소의 **Settings → Pages → Build and deployment → Source**에서 **Deploy from a branch**를 선택합니다.
5. **Branch**를 `main`, 폴더를 `/(root)`로 선택하고 **Save**를 누릅니다.
6. Pages 화면에 표시되는 주소로 접속합니다. 개인 홈페이지 저장소는 보통 `https://사용자명.github.io/`, 일반 저장소는 `https://사용자명.github.io/저장소명/` 형태입니다. 이 사이트는 상대 경로를 사용하므로 두 방식 모두 지원합니다.

공식 안내: [GitHub Pages Quickstart](https://docs.github.com/en/pages/quickstart), [Publishing source 설정](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## 게시 전에 바꿀 내용

- `index.html`의 `[이름 입력]`, `[확인 후 입력]`, `[공개할 이메일 입력]`, `[본인 계정 URL 입력]`을 확인된 실제 정보로 바꿉니다. 연락처를 공개하고 싶지 않다면 해당 행을 삭제해도 됩니다.
- 학력, 활동, 출판·발표, 실제 사용 기술은 **검증된 내용만** 추가합니다. 현재 문구는 빈 기록을 안내하는 표시입니다.
- 프로젝트 상태를 확인한 후 메인 카드와 상세 페이지의 배지 및 설명을 함께 바꿉니다. CSS에는 `status-planned`(기획), `status-active`(진행 중), `status-done`(완료), `status-unverified`(상태 확인 필요)가 준비되어 있습니다.
- 프로젝트 상세 페이지의 기간, 본인 역할, 데이터 출처, 방법, 결과와 자료 링크를 실제 근거에 맞게 채웁니다. 실험 전에는 결과를 빈 상태로 유지합니다.
- CV를 공개하려면 개인정보를 검토한 PDF를 예컨대 `documents/cv.pdf`로 넣고 `index.html`의 CV 표시를 `<a href="documents/cv.pdf" download>CV 다운로드</a>`로 바꿉니다. 파일을 넣기 전에는 링크를 만들지 마세요.
- 이름과 소속이 확정되면 `<title>`, `meta name="description"`, Open Graph 제목·설명도 수정합니다. 실제 공개 주소가 생기면 필요에 따라 canonical URL과 절대 주소의 Open Graph 이미지를 추가합니다.

## 현재 프로젝트 표기 근거

이전 기획 대화에서 **반어 표현 탐지 NLP**와 **AI 마케팅 의사결정 지원 PoC**는 프로젝트 후보로 언급되었지만 기획/진행 중/완료 중 어느 단계인지 확인되지 않았습니다. 따라서 두 항목은 `상태 확인 필요`로 표시합니다. **전주시 공공데이터 기반 AI 리빙랩**은 `주제 검토·기획`으로 언급되어 `기획`으로 표시합니다. 이미지들은 실제 결과 화면이나 실험 그래프가 아닌 추상 일러스트입니다.

## 로컬에서 열기

`index.html`을 브라우저에서 열면 됩니다. 링크와 화면을 실제 배포 환경처럼 확인하려면 이 폴더에서 간단한 정적 서버를 실행할 수도 있습니다(예: `python -m http.server 8000`). 외부 폰트, CDN, API, 빌드 도구는 사용하지 않습니다.

## 접근성과 화면 크기

의미 있는 제목 구조, 본문 바로 가기, 키보드 포커스 표시, 모바일 메뉴의 상태 표기, 프로젝트 필터의 누름 상태, 이미지 대체 텍스트, 동작 줄이기 설정을 포함합니다. 휴대폰·태블릿·데스크톱 너비에 맞춰 배치가 변경됩니다.
