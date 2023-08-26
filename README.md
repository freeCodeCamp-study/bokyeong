> 아래의 링크에 있는 자바스크립트 40제를 구현하고 있습니다.   
> 구현된 기능들은 폴더 별로 다르게 저장되어 있고, 미리보기 및 주요 개념은 아래에 따로 작성해두었습니다.   
> (주요 개념은 아래 링크에서 언급된 것으로, 해당 개념을 필수로 사용하여 구현했습니다.)   
> 링크 : [초보자를 위한 40가지의 자바스크립트 프로젝트](https://www.freecodecamp.org/korean/news/javascript-projects-for-beginners)   

***   
자바스크립트 40제   
=============   
   
**첫번째 예제의 미리보기는 색이 빠르게 바뀝니다. 주의하시기 바랍니다.**   
   
## [01. Color Flipper](https://github.com/hungerbk/freeCodeCamp-study/tree/main/01.ColorFlipper)
![Apr-26-2023 16-28-55](https://user-images.githubusercontent.com/43366461/234501811-5c3f367f-bb00-4cfa-a8c9-8732fc17e908.gif)
   
- 버튼을 클릭하면 배경색이 바뀌고 해당하는 배경색의 이름이 화면에 표시됨
- 현재 배경색과 선택된 배경색을 비교하여 둘이 같은 경우 함수를 다시 실행하도록 구현함 (같은 색으로 바뀌는 경우, 겉으로 보기에는 함수가 제대로 실행되지 않은 것처럼 보임)
- 색 정보가 담긴 리스트를 만든 뒤, 함수를 실행하면 랜덤으로 리스트의 요소를 반환함
    
### 주요 개념
- arrays
- document.getElementById()
- document.querySelector()
- addEventListener()
- document.body.style.backgroundColor
- Math.floor()
- Math.random()
- array.length
***   
## [02. Counter](https://github.com/hungerbk/freeCodeCamp-study/tree/main/02.Counter)
![Apr-26-2023 16-37-27](https://user-images.githubusercontent.com/43366461/234503794-e0e49fa1-f79a-401a-a5de-bf3590710452.gif)
   
- 버튼을 클릭하면 숫자의 크기가 증가, 감소, 초기화되도록 구현
- 숫자의 크기를 비교하여 숫자의 글자색이 다르게 보이도록 구현
- currentTarget 속성을 이용하여 하나의 함수에 여러 기능을 한번에 작성
- classList를 사용하여, class 추가/삭제를 통해 글자 색이 바뀌도록 구현

### 주요 개념
- document.querySelectorAll()
- forEach()
- addEventListener()
- currentTarget 속성
- classList
- textContent
***   
## [03. Review Carousel](https://github.com/hungerbk/freeCodeCamp-study/tree/main/03.reviewCarousel)
![Jul-17-2023 22-58-17](https://github.com/hungerbk/freeCodeCamp-study/assets/43366461/915d64ae-9a4b-41d2-86fd-eece4c7908a5)

- 여러 리뷰 객체의 정보가 있는 리뷰 배열을 생성   
- prevButton을 클릭하면 이전 리뷰가 화면에 보이도록 구현
- nextButton을 클릭하면 다음 리뷰가 화면에 보이도록 구현
- randomButton을 클릭하면 랜덤 리뷰가 화면에 보이도록 구현 (단, 현재 보이는 리뷰와 일치하지 않는 리뷰로만 변경)

### 주요 개념
- 객체
- DOMContentLoaded
- addEventListener()
- array.length
- textContent

***   
## [04. 반응형 내비게이션바 만들기](https://github.com/freeCodeCamp-study/bokyeong/tree/main/04.responsiveNavbar)
![Aug-24-2023 23-12-07](https://github.com/hungerbk/freeCodeCamp-study/assets/43366461/3d9b88de-6baa-4814-aba0-7e31259ded94)

- toggle을 이용하여 반응형 내비게이션 구현
- 내비게이션 바를 숨긴 뒤, 너비에 따라 다른 스타일이 보이게 구현

### 주요 개념
- document.querySelector()
- addEventListener()
- classList.toggle()

### 해결해야 하는 문제
- 아이콘 이미지를 svg를 사용했는데, hover 했을 때는 색상이 변하지만 focus했을 때는 변하지 않음 (css의 filter 이용)

  ![Aug-24-2023 22-32-28](https://github.com/hungerbk/freeCodeCamp-study/assets/43366461/9c6a42d2-6880-49a9-a9c3-6bb4819bedbd)

- 모바일 햄버거 바를 클릭한 경우, 원래대로 돌아오지 않음...

  ![Aug-24-2023 22-35-51](https://github.com/hungerbk/freeCodeCamp-study/assets/43366461/8da4fa45-3ac3-4d2d-862c-d900224104be)

***
## [05. 사이드바 만들기](https://github.com/hungerbk/freeCodeCamp-study/tree/main/05.sidebar)
![Aug-26-2023 22-40-14](https://github.com/hungerbk/freeCodeCamp-study/assets/43366461/e3743172-95e5-40e2-ad59-de6c893ab601)


- classList.toggle() 및 classList.remove()를 이용하여 사이드바 제어
- toggle 버튼을 클릭하면 show-sidebar 클래스를 토글하고, close 버튼을 클릭하면 show-sidebar 클래스를 제거
- transform을 이용하여 show-sidebar 제어
  ```css
  .sidebar {
   tranform: translate(-100%);
   transition: all 0.5s ease;
   }

  .show-sidebar {
   transform: translate(0);
  }
  ```
- 화면 크기에 따라 사이드바의 크기 조절

### 주요개념
- document.querySelector()
- addEventListener()
- classList.toggle()
