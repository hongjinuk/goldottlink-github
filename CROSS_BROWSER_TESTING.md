# 웹사이트 크로스 브라우저 테스트 가이드

## 📋 테스트 개요

goldottlink 웹사이트가 다양한 브라우저와 기기에서 올바르게 작동하는지 확인하기 위한 테스트 가이드입니다.

## 🌐 테스트 대상 브라우저

### 데스크톱 브라우저
1. **Google Chrome** (최신 버전)
   - Windows 10/11
   - macOS
   - Linux (Ubuntu)

2. **Mozilla Firefox** (최신 버전)
   - Windows 10/11
   - macOS
   - Linux (Ubuntu)

3. **Microsoft Edge** (최신 버전, Chromium 기반)
   - Windows 10/11
   - macOS

4. **Safari** (최신 버전)
   - macOS
   - iPadOS

5. **Opera** (선택적)
   - Windows 10/11
   - macOS

### 모바일 브라우저
1. **Chrome Mobile**
   - Android 10+

2. **Safari Mobile**
   - iOS 14+

3. **Samsung Internet**
   - Android 10+

4. **Firefox Mobile** (선택적)
   - Android 10+

## 📱 테스트 대상 기기

### 데스크톱
- 해상도: 1920x1080 (Full HD)
- 해상도: 1366x768 (HD)
- 해상도: 2560x1440 (QHD)
- 해상도: 3840x2160 (4K)

### 태블릿
- iPad (1024x768)
- iPad Pro (1366x1024)
- Android Tablet (800x1280)

### 모바일
- iPhone SE (375x667)
- iPhone 12/13/14 (390x844)
- iPhone 14 Pro Max (430x932)
- Samsung Galaxy S21+ (412x915)
- Google Pixel 6 (412x915)

## ✅ 테스트 체크리스트

### 1. 페이지 로딩 및 렌더링

#### 모든 페이지 (공통)
- [ ] 페이지가 3초 이내에 로드됨
- [ ] 모든 이미지가 올바르게 표시됨
- [ ] 폰트가 올바르게 로드됨
- [ ] 색상이 일관되게 표시됨
- [ ] 레이아웃이 깨지지 않음

#### index.html (랜딩 페이지)
- [ ] 히어로 섹션이 올바르게 표시됨
- [ ] 기능 카드가 그리드로 정렬됨
- [ ] CTA 버튼이 잘 보임
- [ ] 스크롤 애니메이션 작동 (있는 경우)

#### features.html (기능 소개)
- [ ] 기능 목록이 올바르게 표시됨
- [ ] 스크린샷/이미지가 로드됨
- [ ] 탭 전환이 작동함

#### login.html & register.html (인증)
- [ ] 소셜 로그인 버튼이 올바르게 표시됨
- [ ] Google 아이콘이 정확히 렌더링됨
- [ ] Facebook 버튼 색상이 정확함
- [ ] 구분선(divider)이 올바르게 표시됨
- [ ] 폼 입력 필드가 정상 작동함

#### dashboard.html (대시보드)
- [ ] 통계 카드가 올바르게 표시됨
- [ ] Chart.js 차트가 모두 로드됨
- [ ] 파이 차트가 정확히 렌더링됨
- [ ] 라인 차트가 정확히 렌더링됨
- [ ] 막대 그래프가 정확히 렌더링됨
- [ ] 차트 레전드가 올바르게 표시됨
- [ ] 차트 툴팁이 작동함

#### contact.html (문의)
- [ ] 문의 폼이 올바르게 표시됨
- [ ] Select 드롭다운이 작동함
- [ ] Textarea가 올바르게 크기 조정됨
- [ ] 제출 버튼이 작동함

### 2. 반응형 디자인

#### 데스크톱 (1920px+)
- [ ] 내비게이션 메뉴가 가로로 표시됨
- [ ] 콘텐츠가 중앙 정렬됨 (max-width 적용)
- [ ] 그리드가 3-4열로 표시됨

#### 태블릿 (768px - 1024px)
- [ ] 그리드가 2열로 조정됨
- [ ] 폰트 크기가 적절함
- [ ] 이미지 크기가 적절함

#### 모바일 (320px - 767px)
- [ ] 내비게이션이 햄버거 메뉴로 변경됨 (구현된 경우)
- [ ] 그리드가 1열로 조정됨
- [ ] 터치 타겟이 44px 이상
- [ ] 가로 스크롤이 발생하지 않음
- [ ] 폰트 크기가 16px 이상

### 3. 대화형 요소

#### 버튼
- [ ] 호버 효과가 작동함 (데스크톱)
- [ ] 클릭 효과가 보임
- [ ] 비활성화 상태가 올바르게 표시됨
- [ ] 로딩 상태가 표시됨 (해당하는 경우)

#### 링크
- [ ] 호버 시 색상 변경됨
- [ ] 방문한 링크 색상이 다름
- [ ] 외부 링크가 새 탭에서 열림

#### 폼
- [ ] 입력 필드 포커스가 작동함
- [ ] 유효성 검사가 작동함
- [ ] 에러 메시지가 표시됨
- [ ] 플레이스홀더가 올바르게 표시됨
- [ ] 자동 완성이 작동함

#### 모달/다이얼로그
- [ ] 모달이 올바르게 열림
- [ ] 배경 오버레이가 표시됨
- [ ] ESC 키로 닫힘 (구현된 경우)
- [ ] 외부 클릭으로 닫힘 (구현된 경우)

### 4. JavaScript 기능

#### 소셜 로그인
- [ ] Google 로그인 버튼 클릭 시 알림 표시
- [ ] Facebook 로그인 버튼 클릭 시 알림 표시
- [ ] 아이콘이 올바르게 렌더링됨

#### 차트 (Chart.js)
- [ ] 차트가 로드됨
- [ ] 애니메이션이 작동함
- [ ] 툴팁이 표시됨
- [ ] 레전드 클릭이 작동함
- [ ] 반응형 크기 조정이 작동함

#### 문의 폼
- [ ] 폼 제출이 작동함
- [ ] 비동기 제출이 작동함 (구현된 경우)
- [ ] 성공 메시지가 표시됨
- [ ] 에러 처리가 작동함
- [ ] 폼이 초기화됨

#### PWA 기능
- [ ] Service Worker가 등록됨
- [ ] 오프라인에서 캐시된 페이지 표시됨
- [ ] 설치 프롬프트가 표시됨 (모바일)
- [ ] 홈 화면에 추가 가능

### 5. 성능

#### 로딩 속도
- [ ] First Contentful Paint < 1.5초
- [ ] Time to Interactive < 3초
- [ ] Total Blocking Time < 300ms
- [ ] Cumulative Layout Shift < 0.1

#### 리소스
- [ ] 이미지가 최적화됨
- [ ] CSS가 최소화됨
- [ ] JavaScript가 최소화됨
- [ ] 불필요한 리소스가 없음

### 6. 접근성 (A11y)

#### 키보드 내비게이션
- [ ] Tab 키로 모든 요소 접근 가능
- [ ] 포커스 표시가 명확함
- [ ] Enter/Space로 버튼 활성화 가능
- [ ] ESC로 모달 닫기 가능

#### 스크린 리더
- [ ] Alt 텍스트가 모든 이미지에 있음
- [ ] ARIA 레이블이 적절히 사용됨
- [ ] 헤딩 구조가 논리적임 (h1 → h2 → h3)
- [ ] 링크 텍스트가 설명적임

#### 색상 대비
- [ ] 텍스트와 배경의 대비비가 4.5:1 이상
- [ ] 중요한 정보가 색상에만 의존하지 않음
- [ ] 링크가 색상 이외의 방법으로 구분됨

### 7. SEO

#### Meta 태그
- [ ] title 태그가 모든 페이지에 있음
- [ ] description 메타 태그가 있음
- [ ] Open Graph 태그가 있음
- [ ] Twitter Card 태그가 있음

#### 구조화된 데이터
- [ ] JSON-LD가 유효함
- [ ] Schema.org 마크업이 있음

#### 기타
- [ ] robots.txt가 접근 가능함
- [ ] sitemap.xml이 접근 가능함
- [ ] Canonical URL이 설정됨
- [ ] 404 페이지가 적절함 (구현된 경우)

## 🛠️ 테스트 도구

### 온라인 도구

1. **BrowserStack** (https://www.browserstack.com/)
   - 실제 기기에서 테스트
   - 모든 주요 브라우저 지원
   - 스크린샷 비교

2. **LambdaTest** (https://www.lambdatest.com/)
   - 클라우드 기반 테스트
   - 실시간 브라우저 테스트
   - 자동화 테스트 지원

3. **CrossBrowserTesting** (https://crossbrowsertesting.com/)
   - 다양한 브라우저 버전
   - 모바일 기기 테스트

### 브라우저 개발자 도구

#### Chrome DevTools
```
F12 또는 Cmd+Opt+I (Mac)

유용한 기능:
- Device Toolbar (Cmd+Shift+M): 반응형 테스트
- Network 패널: 로딩 시간 확인
- Lighthouse: 성능, 접근성, SEO 점수
- Console: JavaScript 오류 확인
```

#### Firefox Developer Tools
```
F12 또는 Cmd+Opt+I (Mac)

유용한 기능:
- Responsive Design Mode (Cmd+Opt+M)
- Accessibility Inspector
- Network Monitor
```

#### Safari Web Inspector
```
Cmd+Opt+I (Mac)

먼저 활성화:
Safari > Preferences > Advanced > Show Develop menu

유용한 기능:
- Responsive Design Mode
- Timeline
- Network
```

### 자동화 테스트 도구

#### Selenium
```javascript
// 예제: Selenium WebDriver
const { Builder, By, Key, until } = require('selenium-webdriver');

async function testLogin() {
    let driver = await new Builder().forBrowser('chrome').build();
    try {
        await driver.get('http://localhost:3000/login.html');
        await driver.findElement(By.id('email')).sendKeys('test@example.com');
        await driver.findElement(By.id('password')).sendKeys('password123', Key.RETURN);
        await driver.wait(until.titleIs('대시보드 - goldottlink'), 5000);
    } finally {
        await driver.quit();
    }
}

testLogin();
```

#### Playwright
```javascript
// 예제: Playwright
const { chromium } = require('playwright');

(async () => {
    const browser = await chromium.launch();
    const page = await browser.newPage();
    await page.goto('http://localhost:3000/');
    await page.screenshot({ path: 'screenshot.png', fullPage: true });
    await browser.close();
})();
```

### 성능 테스트

#### Google Lighthouse
```bash
# CLI 사용
npm install -g lighthouse
lighthouse http://localhost:3000/ --view

# 측정 항목:
# - Performance: 0-100
# - Accessibility: 0-100
# - Best Practices: 0-100
# - SEO: 0-100
# - PWA: Yes/No
```

#### WebPageTest
- URL: https://www.webpagetest.org/
- 전 세계 여러 위치에서 테스트
- 상세한 성능 분석
- 비교 리포트

## 📊 테스트 결과 기록

### 템플릿

```markdown
## 테스트 날짜: YYYY-MM-DD
## 테스터: [이름]

### 테스트 환경
- OS: [Windows 11 / macOS 13 / Android 13]
- 브라우저: [Chrome 120 / Firefox 121 / Safari 17]
- 화면 크기: [1920x1080 / 375x667]

### 테스트 결과

#### ✅ 통과
- 페이지 로딩 정상
- 차트 렌더링 정상
- 반응형 디자인 정상

#### ❌ 실패
- [문제 설명]
- [재현 단계]
- [스크린샷 링크]

#### ⚠️ 주의 필요
- [개선 필요 사항]

### Lighthouse 점수
- Performance: 95
- Accessibility: 98
- Best Practices: 100
- SEO: 100
- PWA: ✓

### 스크린샷
- [링크]

### 추가 메모
- [기타 의견]
```

## 🐛 알려진 이슈 및 해결 방법

### Issue 1: Chart.js가 IE11에서 작동하지 않음
**해결 방법**: IE11은 더 이상 지원하지 않음. 사용자에게 모던 브라우저 사용 권장.

### Issue 2: SVG 아이콘이 Safari에서 깨짐
**해결 방법**: `viewBox` 속성 확인 및 PNG fallback 제공.

### Issue 3: Service Worker가 로컬에서 작동하지 않음
**해결 방법**: HTTPS 필요. 로컬 개발 시 `localhost` 사용.

## 📝 체크리스트 요약

### 우선순위 높음 (필수)
- [ ] Chrome (Desktop & Mobile)
- [ ] Safari (Desktop & Mobile)
- [ ] Firefox (Desktop)
- [ ] Edge (Desktop)
- [ ] 반응형 디자인 (320px ~ 1920px)
- [ ] JavaScript 기본 기능
- [ ] 폼 제출
- [ ] SEO 메타 태그

### 우선순위 중간
- [ ] Samsung Internet
- [ ] Opera
- [ ] 키보드 내비게이션
- [ ] 스크린 리더 호환성
- [ ] PWA 기능
- [ ] 성능 최적화

### 우선순위 낮음 (선택)
- [ ] Firefox Mobile
- [ ] 구형 브라우저 (IE11 제외)
- [ ] 극단적 화면 크기 (< 320px, > 4K)

## 🎯 목표 기준

### 성능
- Lighthouse Performance: 90+ 
- First Contentful Paint: < 1.5초
- Time to Interactive: < 3초

### 접근성
- Lighthouse Accessibility: 95+
- WCAG 2.1 Level AA 준수

### SEO
- Lighthouse SEO: 95+
- 모든 주요 메타 태그 포함

### 브라우저 지원
- Chrome: 최신 3개 버전
- Firefox: 최신 3개 버전
- Safari: 최신 2개 버전
- Edge: 최신 3개 버전

## 📞 문의

테스트 중 문제 발견 시:
- GitHub Issues: [링크]
- 이메일: support@goldottlink.com
- 문의 폼: contact.html

---

**문서 작성**: AI-Work-Project Team  
**최종 업데이트**: 2026-02-15  
**버전**: 1.0
