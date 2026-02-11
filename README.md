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
- 기본적으로 Vite 개발 서버가 실행되며, 브라우저에서 실시간 확인 가능합니다.

### 3. 프로덕션 빌드
```bash
npm run build
```

### 4. 빌드 결과 미리보기
```bash
npm run start
```

---

## 5) 활용 방안

이 템플릿은 아래와 같은 시나리오에서 빠르게 활용할 수 있습니다.

1. **사내 운영/관리자 페이지 구축**
   - 회원/주문/상품/문의 관리 등 Backoffice UI 초안 제작
2. **SaaS Admin MVP 제작**
   - 초기 제품 단계에서 빠르게 관리자 화면 구성
3. **디자인 시스템 프로토타이핑**
   - 컴포넌트 단위(버튼, 폼, 모달, 테이블)로 화면 정책 검증
4. **프론트엔드 실습/온보딩 자료**
   - Tailwind + Vite + Vanilla JS 구조 학습용 샘플
5. **백엔드 템플릿 결합**
   - Django, Spring, Laravel, Express 등 서버 템플릿 엔진과 연결해 사용

---

## 6) 커스터마이징 가이드

- **테마/디자인 변경**: `tailwind.config.js`, `src/scss/*` 수정
- **컴포넌트 동작 변경**: `src/js/components/*` 수정
- **페이지별 기능 추가**: `src/js/custom/*`에 기능 추가 후 해당 HTML에 연결
- **정적 데이터 교체**: `src/json/*`를 API 응답 데이터로 교체

---

## 7) 배포 가이드

`npm run build` 실행 후 생성되는 `dist/` 폴더를 정적 호스팅에 배포하면 됩니다.

- 예: **Nginx**, **AWS S3 + CloudFront**, **Netlify**, **Vercel(Static)**

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
