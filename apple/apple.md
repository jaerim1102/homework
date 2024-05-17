# apple 제품 카드

## 1. 반응형 구현 결과
<img src="./apple.gif"></img>

## 2. 마크업
div로 모든 section을 감싸고 grid 효과를 줄 수 있도록 grid-container라는 class를 부여했습니다.
각 카드들은 section으로 마크업하고, 대제목에 h1, 부제목에 h2, 출시일 추후 공개 텍스트는 p로 마크업했습니다.
각 버튼들은 div로 묶어 그룹핑하고, 각기 다른 색상을 부여할 수 있도록 class 요소를 추가했습니다.

## 3. 스타일링

``` 
  .grid-container {
   display: grid;
   grid-template-columns: repeat(2, 1fr);
}
```
데스크탑 화면에서 하단 4개의 섹션이 둘둘로 나뉘어져야 했으므로 하단 4개의 섹션에 grid-column: span 1;를 부여하고, 나머지 섹션에는 span 2을 주어 화면에 꽉 차도록 했습니다.
1024px 미만 화면에서 하단 4개의 섹션도 화면에 꽉 차야 했으므로

```
@media (max-width: 1024px)
```

속에서 4, 5, 6, 7번째 섹션 또한 grid-column: span 2;를 주었습니다.


background-image는 

```
background-image: image-set(url('image.png') 1x, url('image@2x.png') 2x, url('image@3x.png') 3x);
```

image-set을 사용해 해상도에 따라 이미지를 제공할 수 있도록 하였고,

```
   background-repeat: no-repeat;
   background-size: cover;
   background-position: center;
```

속성을 주어 화면에 꽉 차도록 하였습니다.


## 4. 과제 후기
- 변수를 직접 사용해 보는 건 처음이라 헷갈렸지만 적응하면 훨씬 편하게 사용할 수 있을 것 같습니다.

- 슬비쌤 영상에서는 h2(부제목) 텍스트도 반응형으로 줄바꿈이 되던데...
span 요소로 h2를 두르고 display: block;을 주면 쉽게 해결할 수 있을 줄 알았는데 마음처럼 되지 않아서 결국 구현하지 못했습니다. ㅜㅜ
