# My Hub — GitHub Pages 배포 가이드

## 파일 구조
```
myhub-gh-pages/
  └── index.html    ← 이 파일 하나만 있으면 됩니다
```

## 배포 방법 (5분이면 완료)

### 1. GitHub 저장소 만들기
1. https://github.com/new 접속
2. Repository name: `my-hub` (원하는 이름)
3. **Public** 선택
4. "Create repository" 클릭

### 2. 파일 업로드
1. 생성된 저장소 페이지에서 "uploading an existing file" 클릭
2. `index.html` 파일을 드래그 앤 드롭
3. "Commit changes" 클릭

### 3. GitHub Pages 활성화
1. 저장소 → **Settings** 탭
2. 왼쪽 메뉴에서 **Pages** 클릭
3. Source: **Deploy from a branch**
4. Branch: **main** / **(root)** 선택
5. **Save** 클릭

### 4. 접속
1~2분 후 아래 주소로 접속 가능:
```
https://[내GitHub아이디].github.io/my-hub/
```

## 사용법

### 할 일
- **+ 추가** 버튼으로 새 할 일 생성
- 체크박스 클릭으로 완료 처리
- 카테고리 분류, 우선순위, 마감일 설정 가능

### 뉴스 허브
- **+ 추가** → URL 입력 → **자동 채우기** 버튼
- AI가 제목, 설명, 썸네일, 카테고리를 자동 분석
- (자동 채우기는 Anthropic API 키가 필요합니다. 없으면 수동 입력)

### 카테고리 관리
- 사이드바(데스크톱) 또는 필터 패널(모바일)에서 **편집** 클릭
- 메인 카테고리: 이름, 색상 변경, 추가, 삭제
- 서브 카테고리: 메인 아래 하위 분류 추가/편집/삭제

### 리마인더
- 7일 이상 확인하지 않은 할 일/뉴스 자동 감지
- 하단 탭바(모바일) 또는 사이드바에 빨간 배지 표시

## 데이터 저장
- 모든 데이터는 브라우저의 localStorage에 저장됩니다
- 같은 브라우저에서 접속하면 데이터가 유지됩니다
- 브라우저 데이터를 삭제하면 초기화되니 주의하세요

## 자동 채우기 기능 (선택사항)
뉴스 URL 자동 분석 기능을 사용하려면 Anthropic API 키가 필요합니다.
현재 코드에서는 API 키 없이 호출하므로, 실제 사용 시에는 index.html 내에서
`api.anthropic.com` 호출 부분에 API 키를 추가하거나,
별도 백엔드 프록시를 사용해야 합니다.

자동 채우기 없이도 수동으로 제목, 설명, 썸네일 입력은 정상 동작합니다.

## 업데이트
index.html 파일을 수정한 후 GitHub에 다시 업로드하면 자동 반영됩니다.
