1. 상태 정보가 될 div와 아바타 이미지를 같은 div로 묶어줍니다.
2. 조건에 있는 대로 img에 width, height, padding 속성을 줍니다.
3. img를 둥글게 만들기 위해 border-radius 속성을 줍니다.
4. 상태 정보 div의 색깔 구분을 위해 각 offline, online 클래스를 줍니다. 각각 다른 background-color를 입힙니다.
5. 상태 정보 div가 img 위에 올 수 있도록 position: absolute;를 줍니다. margin 속성을 이용해 위치를 잡아 줍니다.
6. display: flex; 속성을 통해 .group div들이 가로로 정렬되게 합니다.
7. float: left; 속성을 통해 .group1과 .group2가 위아래로 정렬되게 합니다.
8. @supports(display: flex)으로 flex가 지원되는 환경의 레이아웃을 만듭니다.
9. .group에 flex-direction: column;을 주어서 하위 div가 세로로 정렬되게 하고, .group1에 order: 2; .group2에 order: 1;을 주어서 정렬 순서가 바뀌도록 합니다.