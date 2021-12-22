# display와 visibility



## display

+ **요소의 렌더링 박스 유형**을 결정하는 속성

  태그마다 고유하게 가지고 있는 렌더링 박스의 속성을 변경할 수 있음.

  

```css
display: value;
```

+ 속성값
  + **default: 요소마다 다름**
  + **none**: 요소가 렌더링되지 않음
  + **inline**: inline level 요소처럼 렌더링
  + **block**: block level 요소처럼 렌더링
  + **inline-block**: inline level 요소처럼 배치되고, block level 요소의 성질을 가지는 형태로 렌더링
    + inline-block은 width, height 값을 가질 수 있다. inline은 width와 height가 auto.
  + 이외 list-item, flex, inline-flex, table, table-cell 등이 있다.



##### display와 box-model의 관계

|     display      | width | height | margin | padding | border |
| :--------------: | :---: | :----: | :----: | :-----: | :----: |
|    **block**     |   O   |   O    |   O    |    O    |   O    |
|    **inline**    |   X   |   X    | 좌우 ★ |   O ★   |  O ★   |
| **inline-block** |   O   |   O    |   O    |    O    |   O    |

+ ★ **inline 요소의 padding, border는** inline box에 영향을 주지 못하여, **부모 요소의 박스에  반영되지 않는다.**  따라서 **부모 요소의 높이는 inline 요소의 컨텐츠 높이**에 따라 변하는 것을 확인할 수 있다. 그러므로 **inline 요소의 padding, border 속성**은 실제로는 상하에도 적용되지만, **좌우에만 적용되는 것처럼 보일 수 있다.**
+ 또 padding과 border는 인접한 inline box에도 반영되지 않아, 콘텐츠가 겹칠 수 있기 때문에, 실무에서 잘 사용하지 않는다.





## visibility

+ **요소의 화면 표시 여부**를 지정하는 속성



```css
visibility: visible | hidden | collapse | initial | inherit;
```

+ 속성값
  + **default: visible**
  + **visible**: 화면에 표시
  + **hidden**: 화면에 표시되지 않으나 화면에서 자신의 공간, 박스 영역(margin까지)은  차지함
  + **collapse**: 테이블 관련 요소에만 지정 가능, 셀 간의 경계를 무시하고 숨김.



> ##### 💡 visibility: hidden과 display: none의 차이점
>
> + **display** 값을 **none**으로 지정하면, 요소가 **아예 렌더링 되지 않아 DOM에 존재하지 않는다.**
> + **visibility** 값을 **hidden**으로 지정하면, 요소가 **보이지 않을 뿐, 렌더링되어 화면에 공간을 가지고 있고 DOM에 존재**한다. 스크린 리더기가 해당 영역의 내용을 읽어준다.
> + ***화면에 보이지는 않지만 제공해야 하는 내용**은 display: none이 아닌 **visibility: hidden**을 사용한다!*



