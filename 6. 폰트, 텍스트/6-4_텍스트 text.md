# text



## text-indent

+ **텍스트 문단 첫 줄 들여쓰기를 지정**하는 속성

```css
text-indent: length | initial | inherit;
```

+ 속성값
  + **default : 0**
  + **length** : px, em 등 고정 수치로 지정. 음수 가능
  + **% percent** : 텍스트를 포함하는 컨테이너 블록, 부모의 width를 기준으로 계산된 퍼센트 값 지정



## text-decoration

+ **텍스트의 장식**을 지정하는 단축 속성
  + 해당 속성을 지정한 요소의 **자식 요소가 float 속성값을 가지는 경우, 상속 해제**
  + 해당 속성을 지정한 요소의 **자식 요소가 position : absolute인 경우, 상속 해제**

```CSS
text-decoration: text-decoration-line text-decoration-color text-decoration-style | initial | inherit;
```

+ **default 속성값 : none currentColor solid**



### text-decoration-line

+ 텍스트 **꾸밈의 종류를 지정**하는 속성
+ 속성값
  + **none** : 텍스트 꾸밈 없음 (default)
  + **underline** : 밑줄
  + **overline** : 윗줄
  + **line-through** : 텍스트 중간을 지나는 줄



### text-decoration-color

+ 텍스트 **꾸밈의 색상을 지정**하는 속성
+ default 속성값 : currentColor



### text-decoration-style

+ **꾸밈에 사용되는 선 스타일**을 지정하는 속성
+ 속성값
  + **solid** : 한 줄 (기본값)
  + **double** : 이중선
  + **dotted** : 점선
  + **dashed** : 파선
  + **wavy** : 물결

