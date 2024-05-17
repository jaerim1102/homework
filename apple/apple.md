# apple 제품 카드

## 1. 반응형 구현 결과

## 2. 마크업
div로 모든 section을 감싸고 grid 효과를 줄 수 있도록 grid-container라는 class를 부여했습니다.
각 카드들은 section으로 마크업하고, 대제목에 h1, 부제목에 h2, 출시일 추후 공개 텍스트는 p로 마크업했습니다.
각 버튼들은 div로 묶어 그룹핑하고, 각기 다른 색상을 부여할 수 있도록 class 요소를 추가했습니다.

## 3. 스타일링

  .grid-container {
   display: grid;
   grid-template-columns: repeat(2, 1fr);
}
