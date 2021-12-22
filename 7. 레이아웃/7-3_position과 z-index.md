# position과 z-index



## position

+ **요소의 위치를 정하는 방법**을 지정하는 속성



```css
position: static | absolute | fixed | relative | sticky | initial | inherit;
```

+ 속성값
  + **default: static**
  + **static**
    + 보통의 흐름(normal-flow)으로 배치
    + **offset 값이 적용되지 않음**
  + **relative**
    + 상대위치
    + **요소가 원래 있어야 할 위치를 기준**으로 offset에 따라 배치
    + 보통의 흐름(normal-flow)으로 배치
    + 부모 요소의 position 속성에 영향을 받지 않음
    + 주변 요소에 영향을 주지 않으면서 offset 값으로 이동
  + **absolute**
    + 절대위치
    + **static을 제외한 position 값을 가지는 부모 요소를 기준**으로 offset에 따라 배치
      + 부모 요소가 static인 경우, static이 아닌 가장 가까운 조상 요소를 기준으로 삼는다.
      + **offset의 기준은 기준이 되는 조상 요소의 padding 영역**에 있다.
  + **fixed**
    + 고정위치
    + **뷰포트**, 브라우저 창을 기준으로 offset에 따라 배치
    + 화면 **스크롤에 관계없이 화면의 정해진 위치에 요소가 나타난다.**
    + 부모 요소의 position, 위치에 영향을 받지 않는다.



> 💡 **inline 요소에 absolute, fixed 속성**을 주는 경우, 해당 요소의 **display 값은 block으로 변경**된다. aboluste, fixed 속성을 가진 요소는 block-level이므로 **box-model 관련 속성도 모두 선언할 수 있게 된다.**

> 💡 보통의 흐름 (normal-flow)
>
> + 일반적인 상황에서 각 요소들이 성질에 따라 배치되는 순서, 문서의 흐름.
> + 예를 들어, block 레벨 요소는 상하로, inline 레벨 요소는 좌우로 배치되는 것.





## offset

+ **기준으로부터 상하좌우에 대한 좌표값**

```css
top|bottom|left|right: auto|length|initial|inherit;
```



> 💡
>
> + **offset 값에 따른 변화가 나타나지 않는다면, position이 제대로 선언되었는지 확인**하고 발견할 줄 알아야 한다.
>   + **static은 offset 적용 안 됨**
> + **어디를 기준으로 요소에 offset을 주는 것이 더 좋은지 고민하며 속성을 선언**한다.





## z-index

+ **요소가 쌓이는 순서**를 지정하는 속성

> 💡 
>
> + position이 **static이 아닌 경우에 지정 가능!** 
> + z-index가 **지정되지 않은 경우, 요소의 생성 순서(코드 상 순서)에 따라 요소들이 쌓인다.**



```css
z-index: auto | number | initial | inherit;
```

+ 속성값
  + **default: auto**
  + **auto**: 쌓임 순서를 부모와 동일하게 설정 (기본값)
  + **number**: 해당 수치로 쌓임 순서를 설정한다. 큰 값이 가장 위로 올라옴. 음수 사용 가능.



![](C:\Users\Soyi\Documents\Projects\html_css\images\z-index.png)

+ **부모 요소에 z-index 값이 있을 경우, 부모 요소 내에서만 자식 요소의 z-index 값이 의미를 가진다.** 💡
  + 요소 4의 z-index는 부모 요소 3의 쌓임 맥락 내에서 유효하다.
    + 요소 4는 요소 1보다 z-index 값이 크지만, 부모 요소인 3의 z-index 값이 요소 1의 z-index 값보다 작으므로, 요소 4는 요소 1 아래에 렌더링 된다.
  + 요소 5의 z-index는 부모 요소 3의 쌓임 맥락 내에서 유효하다.
    + 요소 5는 요소 2보다 z-index 값이 작지만, 부모 요소인 3의 z-index 값이 요소 2의 z-index 값보다 크기 때문에, 요소 5는 요소 2 위에 렌더링 된다.

