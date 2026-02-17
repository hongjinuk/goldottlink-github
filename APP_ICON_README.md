# goldottlink App Icon

## 📱 앱 아이콘 디자인

### 디자인 컨셉
- **메인 요소**: 링크 체인 아이콘 (연결성을 상징)
- **컬러 스킴**: 
  - 그라데이션 배경: `#667eea` → `#764ba2` (보라색 계열)
  - 링크 아이콘: 화이트 (`#ffffff`)
  - 연결선: 그린 그라데이션 (`#48bb78` → `#38a169`)
- **OTT 배지**: 명확한 앱 목적 표시

### 파일 구성

#### 1. 소스 파일
- `app-icon.svg` - 벡터 소스 파일 (512x512)
- 필요한 크기로 자유롭게 확대/축소 가능
- 품질 손실 없음

#### 2. 필요한 아이콘 크기

##### Android (Google Play)
```
android_app/app/src/main/res/
├── mipmap-mdpi/ic_launcher.png (48x48)
├── mipmap-hdpi/ic_launcher.png (72x72)
├── mipmap-xhdpi/ic_launcher.png (96x96)
├── mipmap-xxhdpi/ic_launcher.png (144x144)
├── mipmap-xxxhdpi/ic_launcher.png (192x192)
└── Play Store: 512x512 PNG
```

##### iOS (App Store)
```
flutter_app/ios/Runner/Assets.xcassets/AppIcon.appiconset/
├── Icon-20@2x.png (40x40)
├── Icon-20@3x.png (60x60)
├── Icon-29@2x.png (58x58)
├── Icon-29@3x.png (87x87)
├── Icon-40@2x.png (80x80)
├── Icon-40@3x.png (120x120)
├── Icon-60@2x.png (120x120)
├── Icon-60@3x.png (180x180)
├── Icon-76.png (76x76)
├── Icon-76@2x.png (152x152)
├── Icon-83.5@2x.png (167x167)
└── App Store: 1024x1024 PNG
```

##### 웹 (PWA)
```
website/
├── favicon.ico (16x16, 32x32, 48x48)
├── favicon-16x16.png
├── favicon-32x32.png
├── apple-touch-icon.png (180x180)
├── android-chrome-192x192.png
└── android-chrome-512x512.png
```

### 아이콘 생성 방법

#### 옵션 1: 온라인 도구 사용 (추천)
1. **App Icon Generator** (https://appicon.co/)
   - `app-icon.svg` 업로드
   - 플랫폼 선택 (iOS, Android)
   - 모든 크기 자동 생성
   - ZIP 다운로드

2. **Favicon Generator** (https://realfavicongenerator.net/)
   - 웹 파비콘 생성
   - 모든 브라우저 지원
   - manifest.json 자동 생성

#### 옵션 2: Figma/Adobe Illustrator
1. `app-icon.svg` 파일 열기
2. 필요한 크기로 Export
3. 각 플랫폼에 맞게 저장

#### 옵션 3: ImageMagick (커맨드 라인)
```bash
# SVG를 PNG로 변환
convert -background none -size 512x512 app-icon.svg app-icon-512.png

# 다양한 크기 생성
convert app-icon-512.png -resize 48x48 mipmap-mdpi/ic_launcher.png
convert app-icon-512.png -resize 72x72 mipmap-hdpi/ic_launcher.png
convert app-icon-512.png -resize 96x96 mipmap-xhdpi/ic_launcher.png
convert app-icon-512.png -resize 144x144 mipmap-xxhdpi/ic_launcher.png
convert app-icon-512.png -resize 192x192 mipmap-xxxhdpi/ic_launcher.png

# iOS 아이콘
convert app-icon-512.png -resize 1024x1024 ios-1024.png
convert app-icon-512.png -resize 180x180 Icon-60@3x.png

# 파비콘
convert app-icon-512.png -resize 32x32 favicon-32x32.png
convert app-icon-512.png -resize 16x16 favicon-16x16.png
```

### 앱스토어 제출 가이드라인

#### Google Play Store
- **아이콘 크기**: 512 x 512 픽셀
- **파일 형식**: 32비트 PNG (알파 채널 포함)
- **최대 파일 크기**: 1MB 이하
- **가이드라인**:
  - 모든 가장자리에서 최소 1픽셀 여백
  - 그림자나 3D 효과 지양 (Flat 디자인 권장)
  - 배경 투명 불가 (단색 또는 그라데이션)

#### Apple App Store
- **아이콘 크기**: 1024 x 1024 픽셀
- **파일 형식**: PNG (알파 채널 제거)
- **색상 공간**: sRGB 또는 P3
- **가이드라인**:
  - 라운드 코너 자동 적용 (직접 추가 금지)
  - 투명도 불가
  - Full bleed (여백 없이 전체 채우기)

### 디자인 변형 아이디어

1. **라이트 모드**
   - 배경: 밝은 파스텔 색상
   - 아이콘: 어두운 색상

2. **다크 모드**
   - 배경: 어두운 그라데이션
   - 아이콘: 밝은 네온 색상

3. **시즌 테마**
   - 크리스마스: 빨강/초록
   - 할로윈: 주황/검정
   - 봄: 파스텔 핑크/그린

### 브랜딩 가이드라인

#### 색상 팔레트
```css
/* Primary Colors */
--primary-purple: #667eea;
--primary-purple-dark: #764ba2;

/* Secondary Colors */
--secondary-green: #48bb78;
--secondary-green-dark: #38a169;

/* Accent Colors */
--accent-blue: #4299e1;
--accent-pink: #ed64a6;

/* Neutral Colors */
--white: #ffffff;
--gray-100: #f7fafc;
--gray-900: #1a202c;
```

#### 타이포그래피
- **Primary Font**: SF Pro (iOS), Roboto (Android)
- **Weight**: Bold (700) for app name
- **Size**: 앱 이름은 아이콘 하단에 시스템 기본 크기

### 체크리스트

- [ ] SVG 소스 파일 생성 완료
- [ ] Android 아이콘 (모든 density) 생성
- [ ] iOS 아이콘 (모든 크기) 생성
- [ ] 웹 파비콘 생성
- [ ] Play Store 512x512 PNG 준비
- [ ] App Store 1024x1024 PNG 준비
- [ ] 모든 플랫폼에 아이콘 적용
- [ ] 실제 기기에서 테스트
- [ ] 가이드라인 준수 확인

### 참고 자료

- [Android Icon Guidelines](https://developer.android.com/distribute/google-play/resources/icon-design-specifications)
- [iOS Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/app-icons)
- [PWA Icon Guidelines](https://web.dev/add-manifest/)
- [Material Design Icons](https://material.io/design/iconography)

### 연락처

아이콘 디자인 수정이 필요하거나 질문이 있으시면 contact.html을 통해 문의해주세요.

---

**제작**: AI-Work-Project Team  
**날짜**: 2026-02-15  
**버전**: 1.0
