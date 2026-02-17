# goldottlink 정적 웹사이트

이 디렉토리는 goldottlink 프로젝트의 정적 마케팅 웹사이트를 포함합니다.

## 🌐 온라인 접속

**GitHub Pages 배포 URL**: 
```
https://ai-work-project.github.io/goldottlink/
```

이 웹사이트는 main 브랜치에 변경사항이 푸시될 때 자동으로 배포됩니다.

## 📁 파일 구조

```
website/
├── index.html              # 메인 홈페이지
├── features.html           # 기능 소개
├── guide.html              # 사용 가이드
├── faq.html                # FAQ
├── contact.html            # 연락처
├── app.html                # 앱 다운로드
├── login.html              # 로그인 (데모)
├── register.html           # 회원가입 (데모)
├── dashboard.html          # 대시보드 (데모)
├── viewer.html             # 뷰어
├── admin-login.html        # 관리자 로그인
├── admin-dashboard.html    # 관리자 대시보드
├── styles.css              # 스타일시트
├── manifest.json           # PWA 매니페스트
├── service-worker.js       # 서비스 워커
├── robots.txt              # SEO 설정
├── sitemap.xml             # 사이트맵
├── app-icon.svg            # 앱 아이콘
└── favicon.svg             # 파비콘
```

## 🚀 로컬 테스트

웹사이트를 로컬에서 테스트하려면:

### Python 사용
```bash
cd website
python3 -m http.server 8000
```

### Node.js 사용
```bash
cd website
npx http-server -p 8000
```

### VS Code Live Server
1. VS Code에서 `website/` 디렉토리 열기
2. Live Server 확장 설치
3. HTML 파일을 열고 "Go Live" 클릭

그런 다음 브라우저에서 `http://localhost:8000` 접속

## ✨ 주요 기능

### 정적 콘텐츠
- 순수 HTML/CSS/JavaScript
- 백엔드 서버 불필요
- 빠른 로딩 속도
- 무료 호스팅 (GitHub Pages)

### PWA 지원
- 오프라인 접근 가능
- 홈 화면에 설치 가능
- 앱과 같은 경험

### SEO 최적화
- Open Graph 메타 태그
- Twitter Card
- 구조화된 데이터 (JSON-LD)
- 사이트맵 및 robots.txt

### 반응형 디자인
- 모바일 최적화
- 태블릿 지원
- 데스크톱 레이아웃

## 🛠 개발

### 파일 수정
1. HTML/CSS/JS 파일 편집
2. 로컬에서 테스트
3. Git에 커밋 및 푸시
4. GitHub Actions가 자동 배포

### 스타일 수정
- `styles.css`: 공통 스타일
- 각 HTML 파일에 인라인 스타일도 있음

### 새 페이지 추가
1. 새 HTML 파일 생성
2. 기존 페이지의 구조 참고
3. `sitemap.xml`에 추가
4. 네비게이션 메뉴 업데이트

## 📝 중요 사항

### ✅ 이 웹사이트로 가능한 것
- 프로젝트 소개 및 홍보
- 기능 설명 및 데모
- 앱 다운로드 링크
- 문의 및 FAQ
- 문서 및 가이드

### ❌ 이 웹사이트로 불가능한 것
- 실제 사용자 로그인/인증
- 데이터베이스 저장
- 서버 사이드 처리
- API 호스팅

실제 기능이 필요한 경우:
- 백엔드: `../backend/` (Spring Boot)
- 프론트엔드: `../frontend/` (React)
- 모바일 앱: `../android_app/`, `../flutter_app/`

## 🔗 관련 문서

- [GitHub Pages 배포 가이드](../GITHUB_PAGES_GUIDE.md)
- [메인 README](../README.md)
- [API 문서](../docmd/API_DOCUMENTATION.md)

## 📞 지원

문제가 있거나 질문이 있으면:
1. GitHub Issues에 등록
2. 팀에 문의

---

© 2026 goldottlink. Made with ❤️ by AI-Work-Project Team
