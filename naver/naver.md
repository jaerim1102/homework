1. 마크업
input type = email 과 password를 사용하여 이메일 입력란, 비밀번호 입력란을 각각 구현
로그인 버튼은 button 요소를 사용함

input type = checkbox와 label을 사용하여 하단 로그인 상태 유지 요소 마크업
IP 보안 텍스트를 클릭하면 ip-security.html로 이동하도록 a 요소를 사용하여 텍스트 마크업
input type = radio에 on, off 두개의 label을 주어 toggle로 on/off를 작동할 수 있도록 마크업

2. 스타일링

* {
   color: #181818;
   font-size: 1rem;
}
전체 텍스트의 컬러와 font-size가 통일되도록 스타일링 후 조건에 맞춰 요소들을 배치

<!-- 반응형 -->
@media (max-width: 767px)로 모바일 상태 먼저 스타일링함
   form {
      width: calc(100% - 20px);
   }
   으로 form width가 100%가 되게하되, 마진 20Px이 남을 수 있도록 함
   
   하단 section에도 같은 width값을 주고,
      display: flex;
      justify-content: flex-end;
      로 로그인 상태 유지 요소가 왼쪽에 배치되도록 함

.ip는 모바일 상태에서는 보이지 않도록 display: none; 사용

<!-- focus -->
input[type="email"]:focus,
input[type="password"]:focus,
button[class="login"]:focus {
   outline: 1px solid #03cf5d;
}

input[type="email"]:focus,
input[type="password"]:focus {
   background-color: #e9f0fd;

}
이메일, 비밀번호, 로그인 입력창에 focus시 outline과 bgc가 변경되도록 속성 줌


<!-- section -->
하단 section 속 radio와 checkbox의 기본 스타일링을 숨겨야했는데 display: none;을 주면 focus-visible이 작동되지
않는 문제가 있었음.


input[type="radio"],
   input[type="checkbox"]{
      position: absolute;
      appearance: none;
    }

때문에 appearance: none;로 요소를 숨김 처리함

position: absolute; 속성 때문에 클릭 범위가 늘어난 것을
    width, height, margin 값을 활용해 조정함


.check를 클릭하면 이미지가 변경되어야 했기 때문에
      input+label {
         background-size: 24px;
         background-repeat: no-repeat;
         background-image: url('icons/unchecked.svg');
      }

input:checked+label {
         background-size: 24px;
         background-repeat: no-repeat;
         background-image: url('icons/checked.svg');
      }
      를 사용해 input과 label을 체크하면 bg 이미지가 변경되도록 구현함

.onOff를 구현하기 위해 off를 체크하면 숨겨져있는 on label이 보이도록 구현함
