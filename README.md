![notion](https://user-images.githubusercontent.com/110226567/213738417-9f523b25-751f-4518-9c78-78b95bb1041d.png)

# 📄 Notion

Notion 반응형 웹사이트 👉 [Demo](https://imjone.github.io/notion/)
<br><br>

## 📢 프로젝트 소개

### [Notion 공식 웹사이트 클론 코딩]

- Notion 공식 웹 사이트 메인 페이지 UI 클론 코딩
- 부분적인 디자인 수정 및 간단한 애니메이션 구현
- 모바일과 PC 모두 보기 편하도록 반응형으로 작업
<br><br>

## 🗨️ 사용 기술

![HTML](https://img.shields.io/badge/HTML-e34f26?style=flat-square&logo=HTML5&logoColor=white)
![css](https://img.shields.io/badge/CSS-1572b6?style=flat-square&logo=CSS3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?style=flat-square&logo=JavaScript&logoColor=white)
<br><br>

## 📋 주요 기능

### 1. 반응형 작업

- 미디어 쿼리 : PC, 태블릿, 모바일
- 레이아웃 : 사이즈에 맞춰 유연하게 변화하는 레이아웃
- 햄버거 버튼 : 모바일 한정 메인 메뉴 노출 버튼

### 2. 스크롤 애니메이션

- 헤더 & 메뉴바 : 스크롤 시 동적 변화 (box-shadow, height)
- 첫 번째 섹션 (home) : 스크롤값에 따른 투명도 조절
- AOS 라이브러리 : 섹션 등장 애니메이션 (Fade)
- 햄버거 버튼 : 클릭 시 해당하는 섹션으로 부드럽게 스크롤

### 3.  최상단 이동 버튼

- home 섹션의 절반 높이 정도 스크롤 됐을 때 노출
- ⬆️ 버튼 클릭 시 페이지 최상단으로 이동

### 4. 이미지 필터링

- 활용법 카테고리 : 메모, 작업, 보고서, 디자인, 메뉴얼
- 카테고리 클릭 시, 해당하는 활용 예제 이미지 노출

### 5. 템플릿 스와이퍼

- Swiper 라이브러리를 사용한 템플릿 샘플 이미지 슬라이더
- loop 옵션으로 인해 무한 자동 슬라이드
- ◀️ ▶️ 버튼을 클릭하여 수동 슬라이드
<br><br>

## 😊 나의 회고록

### 💧 어려웠던 점 및 개선 사항

반응형 작업이 생각보다 까다로웠다.
이것저것 고려해야 할 사항이 많아서 머리가 깨지는 줄 알았다..
또한 기존에 작성해두었던 제이쿼리 코드를 바닐라 자바스크립트 코드로 변경하는 과정에서
시간이 꽤 지체되는 바람에, 넣고 싶었던 애니메이션 요소들을 몇 개 넣지 못했다.
기획 단계에서 조금 더 세세한 부분들까지 방안을 마련해놓고,
순수 자바스크립트만으로 꾸준히 로직을 작성해 나갔다면 좋았을텐데..
하는 마음에 약간의 아쉬움이 남는다.

### 🔥 배운 점 및 느낀 점

반응형 작업이 깔끔하게 마무리되어 뿌듯하다.
또한 AOS 같은 애니메이션 라이브러리를 처음으로 접해봤는데, 정말 신세계였다.
이런 유용한 라이브러리들을 적절히 활용하여 빠르게 UI를 만들어내고,
내가 원하는 기능 구현에만 집중할 수 있도록 활용법을 익혀놔야겠다.
공식 사이트는 다소 정적인 느낌이지만,
나중에 시간이 된다면 여러 가지 동적인 요소들을 넣어서 심심하지 않게끔
인터랙티브한 나만의 Notion 웹사이트로 재탄생 시켜보고 싶다.
