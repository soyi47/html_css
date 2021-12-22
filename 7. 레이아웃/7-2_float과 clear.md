# float과 clear



## float

+ 요소를 보통의 흐름에서 벗어나게(float) 할지 지정하는 속성
+ **한 요소가, 보통의 흐름(normal flow)에서 벗어나, 부모 컨테이너의 좌우 측을 따라 배치**되면서, 텍스트 및 인라인(inline) 요소가 그 주위를 감싸게 되어야함을 지정하는 속성
+ **주변 텍스트와 인라인 요소가 floatinig 된 요소의 주변을 감싸는** 특징을 가진다.
+ floating된 요소는, **대부분 display 값이 block으로 변경**된다. (예외: inline-table, flex, ...)



```css
float: none | left | right | initial | inherit;
```

+ 속성값
  + **default: none**
  + **none**: float 하지 않음(기본값)
  + **left**: 부모 컨테이너의 좌측으로 float
  + **right**: 부모 컨테이너의 우측으로 float





## clear

+ **floating 된 요소의 영향에서 벗어나도록, floating 요소 주변의 요소에 지정**하는 속성
+ **block-level** 요소에만 적용 가능하다. (block 태그 또는 display: block)



```css
clear: none | left | right | both | initial | inherit;
```

+ 속성값
  + **default: none**
  + **none**: 양쪽으로 floating 요소 허용 (기본값)
  + **left**: 왼쪽으로 floating 요소 허용
  + **right**: 오른쪽으로 floating 요소 허용
  + **both**: 양쪽으로 floating 요소 허용



>  💡 floating 요소의 영향력을 제거하는 방법 **clearfix**를 추가로 알아보자.

