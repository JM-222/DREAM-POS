# 📁 프로젝트 폴더 구조 설명

이 문서는 GitHub에 업로드할 때 각 폴더와 파일의 역할을 설명합니다.

---

## 🗂️ 전체 구조

```
DREAM_POS_GitHub/
│
├── 📄 index.html              ← 메인 파일 (이것만 열면 됨)
├── 📄 README.md               ← 사용 설명서
├── 📄 STRUCTURE.md            ← 이 파일
│
├── 📁 css/                    ← 스타일시트
│   └── styles.css             ← 전체 디자인 (색상, 레이아웃, 애니메이션)
│
├── 📁 js/                     ← JavaScript 로직
│   └── app.js                 ← 애플리케이션 기능 (상품 관리, 결제 등)
│
├── 📁 fonts/                  ← 폰트 파일
│   ├── NanumGothic.ttf        ← 본문 글씨 (일반 텍스트)
│   ├── BlackHanSans.ttf       ← 제목 글씨 (굵은 한글)
│   ├── ShareTechMono.ttf      ← 숫자/데이터 글씨 (고정폭)
│   └── GowunBatang.ttf        ← 보조 글씨 (세리프)
│
├── 📁 images/                 ← 이미지 파일
│   └── logo.png               ← 드림편의점 로고
│
└── 📁 audio/                  ← 음향 효과 파일
    ├── beep.wav               ← 버튼 클릭음
    ├── cash.wav               ← 현금 결제음
    ├── card.wav               ← 카드 결제음
    ├── success.wav            ← 성공 알림음
    └── fail.wav               ← 실패 알림음
```

---

## 📄 각 파일 설명

### `index.html` (메인 파일)
- **역할**: 전체 애플리케이션의 진입점
- **포함 내용**: HTML 구조 + CSS + JavaScript (모두 한 파일에 내장)
- **사용법**: 이 파일을 브라우저에서 열기만 하면 POS 시스템 실행
- **크기**: ~500KB (모든 데이터 포함)

### `css/styles.css` (스타일시트)
- **역할**: 전체 디자인 담당
- **포함 내용**:
  - 색상 정의 (--accent, --danger 등)
  - 레이아웃 (그리드, 플렉스박스)
  - 애니메이션 (스플래시, 결제 화면 등)
  - 반응형 디자인 (모바일/태블릿 최적화)
- **수정 시**: 색상이나 디자인을 바꾸고 싶을 때 이 파일 수정

### `js/app.js` (애플리케이션 로직)
- **역할**: 기능 구현
- **포함 내용**:
  - 상품 데이터 관리
  - 카트 시스템
  - 결제 처리
  - 게임 목표 추적
  - 음향 효과
  - 로컬 스토리지 저장
- **수정 시**: 상품 추가, 기능 변경 시 이 파일 수정

### `fonts/` (폰트 폴더)
- **NanumGothic.ttf**: 기본 글씨체 (일반 텍스트용)
- **BlackHanSans.ttf**: 제목용 굵은 한글 폰트
- **ShareTechMono.ttf**: 숫자와 데이터 표시용 고정폭 폰트
- **GowunBatang.ttf**: 보조 텍스트용 세리프 폰트

**왜 필요한가?**
- 인터넷 연결 없이 오프라인에서도 글씨가 제대로 보이도록
- 각 폰트는 특정 역할에 최적화됨

### `images/` (이미지 폴더)
- **logo.png**: 드림편의점 로고
- 스플래시 화면, 타이틀바, 결제 완료 화면에 표시

**최적화 팁:**
- PNG 형식으로 투명도 지원
- 파일 크기 최소화 (웹 로딩 속도 향상)

### `audio/` (음향 효과 폴더)
- **beep.wav**: 버튼 클릭할 때 나는 소리
- **cash.wav**: 현금 결제 완료 시 나는 소리
- **card.wav**: 카드 결제 완료 시 나는 소리
- **success.wav**: 성공 알림음
- **fail.wav**: 실패 알림음

**주의:**
- WAV 형식 (모든 브라우저 지원)
- 파일 크기 작게 유지 (로딩 빠르게)

---

## 🚀 GitHub에 업로드하는 방법

### 1단계: 폴더 준비
```bash
# 모든 파일이 이 구조로 준비되어 있는지 확인
DREAM_POS_GitHub/
├── index.html
├── README.md
├── STRUCTURE.md
├── css/styles.css
├── js/app.js
├── fonts/
├── images/
└── audio/
```

### 2단계: GitHub 저장소 생성
1. GitHub.com에 로그인
2. "New repository" 클릭
3. Repository name: `DREAM_POS` (또는 원하는 이름)
4. "Create repository" 클릭

### 3단계: 파일 업로드
**방법 1: 웹 인터페이스 (가장 간단)**
1. GitHub 저장소 페이지 열기
2. "Add file" → "Upload files" 클릭
3. 모든 폴더와 파일을 마우스로 드래그해서 놓기
4. "Commit changes" 클릭

**방법 2: 터미널 (고급)**
```bash
cd DREAM_POS_GitHub
git init
git add .
git commit -m "Initial commit: DREAM POS System"
git branch -M main
git remote add origin https://github.com/[username]/DREAM_POS.git
git push -u origin main
```

### 4단계: GitHub Pages 활성화
1. 저장소 Settings 클릭
2. Pages 섹션 찾기
3. Source를 "main" 브랜치로 설정
4. 자동 생성된 URL 사용

---

## 💡 파일 크기 최적화

| 파일 | 크기 | 최적화 팁 |
|------|------|---------|
| index.html | ~500KB | 이미 최적화됨 |
| styles.css | ~50KB | 필요 없음 |
| app.js | ~30KB | 필요 없음 |
| fonts/ | ~200KB | 필요한 폰트만 유지 |
| images/ | ~100KB | PNG 압축 도구 사용 |
| audio/ | ~150KB | MP3로 변환 고려 |

---

## 🔄 파일 수정 시 주의사항

### HTML 수정 금지 ❌
- `index.html`은 수정하지 마세요
- 모든 코드가 한 파일에 내장되어 있습니다

### CSS 수정 가능 ✅
- 색상 변경: `:root` 섹션의 변수 수정
- 레이아웃 변경: 각 클래스의 `width`, `height`, `padding` 수정
- 애니메이션 변경: `@keyframes` 섹션 수정

### JavaScript 수정 가능 ✅
- 상품 추가: `products` 배열에 항목 추가
- 가격 변경: 각 상품의 `price` 값 수정
- 기능 추가: 새로운 함수 작성

---

## 📊 파일 체크리스트

GitHub에 업로드하기 전에 확인하세요:

- [ ] `index.html` 파일 존재
- [ ] `README.md` 파일 존재
- [ ] `css/styles.css` 파일 존재
- [ ] `js/app.js` 파일 존재 (또는 index.html에 내장)
- [ ] `fonts/` 폴더에 4개 폰트 파일 존재
- [ ] `images/` 폴더에 로고 파일 존재
- [ ] `audio/` 폴더에 5개 음향 파일 존재
- [ ] 모든 파일 경로가 올바른지 확인
- [ ] 로컬에서 `index.html` 열어서 정상 작동 확인

---

## 🎯 다음 단계

1. **GitHub에 업로드** → 위의 "GitHub에 업로드하는 방법" 참고
2. **GitHub Pages 활성화** → 자동 배포 URL 생성
3. **카카오톡으로 공유** → URL을 친구들에게 공유
4. **아이패드에서 사용** → Safari에서 열고 "홈 화면에 추가"

---

**준비 완료! 이제 GitHub에 업로드하세요! 🚀**
