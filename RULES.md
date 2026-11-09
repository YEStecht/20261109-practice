# 프로젝트 작업 규칙 (Project Rules)

이 프로젝트는 **Vanilla JavaScript**를 사용하는 **Vite** 프로젝트이며, GitHub에 업로드 후 **Netlify**를 통해 배포됩니다.

모든 작업은 아래 규칙을 준수하여 진행합니다.

---

### 1. 코드 분리 원칙
- HTML, CSS, JavaScript 코드는 각각 분리된 독립 파일로 작성합니다. (인라인 스크립트/스타일 지양)

### 2. 디렉터리 및 파일 구조
- `index.html`: 프로젝트 루트(`root`)에 위치합니다.
- 애플리케이션 소스 코드: CSS 및 JavaScript 파일은 `src/` 폴더 내에 작성합니다.
- 설정 파일: `vite.config.js` 등 모든 환경설정 파일은 프로젝트 루트에 위치합니다.

### 3. 모듈 및 스타일 연결
- JavaScript는 ES 모듈(`type="module"`) 방식으로 연결합니다.
- CSS는 JavaScript 진입점 파일(`src/main.js` 등)에서 `import`하여 Vite 빌드 파이프라인에 포함되도록 합니다.

### 4. 외부 라이브러리 관리
- 외부 JavaScript 라이브러리는 CDN 방식을 사용하지 않고, 반드시 `npm install`을 통해 설치한 뒤 `import`하여 사용합니다.

### 5. 기존 파일 및 설정 보존
- 기존 파일과 설정이 있는 경우 먼저 상태를 확인하고, 필요한 부분만 최소한으로 수정합니다.

---

### 배포 설정 (Netlify)
- **Build command**: `npm run build`
- **Publish directory**: `dist`

