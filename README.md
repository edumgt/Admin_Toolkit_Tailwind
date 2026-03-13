# Admin Toolkit (HTML) 프로젝트 가이드

<div align="center">
  <img src="./src/images/logo.png" height="56" alt="Admin Toolkit 로고" />
  <p><strong>Tailwind CSS 기반 관리자 대시보드 템플릿</strong></p>
</div>

## 1) 프로젝트 소개

Admin Toolkit은 **정적 HTML + Tailwind CSS + Vanilla JavaScript** 조합으로 구성된 관리자(Admin) 대시보드 템플릿입니다.  
대시보드, 이커머스, 이메일, 캘린더, 테이블, 폼, 인증 페이지 등 실제 서비스에 바로 적용 가능한 UI 화면을 제공합니다.

---

## 2) 기술 스택

### Core
- **HTML5**
- **JavaScript (ES Modules)**
- **SCSS (Sass)**
- **Tailwind CSS 3**
- **Vite 4** (개발 서버 / 빌드)

### Build / Formatting
- **PostCSS / Autoprefixer**
- **Prettier + prettier-plugin-tailwindcss**

### 주요 UI/기능 라이브러리
- 차트: **ApexCharts**, **amCharts 5**
- 캘린더: **FullCalendar**
- 에디터: **Quill**
- 데이터테이블: **simple-datatables**
- 파일 업로드: **Dropzone**
- 날짜 선택: **flatpickr**
- Tooltip/Popover: **tippy.js**, **@floating-ui/dom**
- 슬라이더: **Swiper**
- 셀렉트/태그: **Tom Select**, **Tagify**
- 알림/토스트: **toastify-js**
- 아이콘/폰트: **Font Awesome**, **Tabler Icons**, **Boxicons**, **Flag Icons**

---

## 3) 프로젝트 구조

```bash
.
├── src/
│   ├── *.html                # 페이지 템플릿 (대시보드/컴포넌트/앱 화면)
│   ├── js/
│   │   ├── app.js            # 공통 엔트리
│   │   ├── components/       # 재사용 UI 컴포넌트 로직
│   │   └── custom/           # 페이지별 커스텀 동작
│   ├── scss/                 # 전역 및 컴포넌트 스타일
│   ├── images/               # 이미지 에셋
│   └── json/                 # 샘플 데이터
├── .github/workflows/
│   └── deploy-static-site.yml # GitHub Pages 자동 배포 워크플로우
├── tailwind.config.js
├── vite.config.js
└── package.json
```

---

## 4) 설치 및 실행

### 요구사항
- **Node.js 18+** 권장
- **npm** 또는 **yarn**

### 1. 의존성 설치
```bash
npm install
```

### 2. 개발 서버 실행
```bash
npm run dev
```

### 3. 프로덕션 빌드
```bash
npm run build
```

### 4. 빌드 결과 미리보기
```bash
npm run start
```

---

## 5) 정적 웹사이트 배포 (GitHub Pages)

이 저장소는 **GitHub Actions + GitHub Pages**로 자동 배포되도록 구성되어 있습니다.

### 배포 방식
1. `main` 브랜치에 push
2. Actions에서 `npm ci` → `npm run build -- --mode github-pages` 수행
3. `dist/` 결과물을 GitHub Pages에 배포

### 배포 URL
- `https://<github-username>.github.io/Admin_Toolkit_Tailwind/`

> 첫 배포 전에는 GitHub 저장소 설정(Settings → Pages)에서 Source를 **GitHub Actions**로 설정하세요.

---

## 6) Playwright 화면 캡처 (5종)

아래 이미지는 docker playwright 환경에서 캡처한 주요 화면입니다.

### 1. Dashboard (Analytics)
![Dashboard Screenshot](browser:/tmp/codex_browser_invocations/d7e9fb9d8525912a/artifacts/docs/screenshots/index.png)

### 2. Ecommerce
![Ecommerce Screenshot](browser:/tmp/codex_browser_invocations/d7e9fb9d8525912a/artifacts/docs/screenshots/ecommerce.png)

### 3. Email
![Email Screenshot](browser:/tmp/codex_browser_invocations/d7e9fb9d8525912a/artifacts/docs/screenshots/email.png)

### 4. Calendar
![Calendar Screenshot](browser:/tmp/codex_browser_invocations/d7e9fb9d8525912a/artifacts/docs/screenshots/calendar.png)

### 5. Form Layout
![Form Layout Screenshot](browser:/tmp/codex_browser_invocations/d7e9fb9d8525912a/artifacts/docs/screenshots/form-layout.png)

---

## 7) 커스터마이징 가이드

- **테마/디자인 변경**: `tailwind.config.js`, `src/scss/*` 수정
- **컴포넌트 동작 변경**: `src/js/components/*` 수정
- **페이지별 기능 추가**: `src/js/custom/*`에 기능 추가 후 해당 HTML에 연결
- **정적 데이터 교체**: `src/json/*`를 API 응답 데이터로 교체

---

## 8) 스크립트 목록

```json
{
  "dev": "vite",
  "build": "vite build --emptyOutDir",
  "start": "vite preview",
  "format": "prettier --write \"src/**/*.{js,css,scss,html}\""
}
```

---

## 9) 라이선스

본 프로젝트는 `MIT` 라이선스를 따릅니다.
