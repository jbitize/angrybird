# Angry Bird 게임 구현 계획

## 개요
- 단일 `index.html` 파일
- Matter.js CDN 물리엔진
- 아이폰 사파리 터치 지원

## 기술 스택
- HTML5 Canvas
- Matter.js (CDN: `https://cdnjs.cloudflare.com/ajax/libs/matter-js/0.20.0/matter.min.js`)
- 순수 JavaScript (터치 + 마우스 이벤트)

## 게임 구성요소

### 1. 화면 레이아웃
- 반응형 전체화면 캔버스 (viewport 기준)
- 좌측: 새 발사대 (슬링샷)
- 우측: 블록 + 돼지 구조물
- 하단: 지면

### 2. 슬링샷 메커니즘
- 터치/마우스로 새를 잡아당김 (드래그)
- 고무줄 시각적 표현 (라인 렌더링)
- 놓으면 당긴 반대 방향으로 발사
- 최대 당김 거리 제한

### 3. 물리 오브젝트
- **새 (Bird)**: 원형, 높은 반발력, 발사체
- **돼지 (Pig)**: 원형, 타격 시 제거 (일정 충격량 이상)
- **블록 (Block)**: 사각형, 나무/돌 재질, 물리 반응
- **지면 (Ground)**: 정적 바디
- **슬링샷 기둥**: 시각적 표현

### 4. 게임 로직
- 새 3마리 제공
- 모든 돼지 제거 시 승리
- 새 소진 시 패배
- 발사 후 일정 시간 뒤 다음 새 준비
- 리스타트 버튼

### 5. 시각 표현
- Canvas 2D로 직접 렌더링 (Matter.js Render 미사용)
- 새: 빨간 원 + 눈/부리
- 돼지: 초록 원 + 얼굴
- 블록: 갈색/회색 사각형
- 슬링샷: Y자 형태
- 배경: 하늘색 그라데이션 + 잔디

### 6. 아이폰 사파리 대응
- `<meta name="viewport">` 설정
- `touch-action: none` (스크롤 방지)
- `touchstart/touchmove/touchend` 이벤트
- `user-select: none`, `overscroll-behavior: none`
- 상단바/하단바 고려한 레이아웃
