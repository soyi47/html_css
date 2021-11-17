# align 정렬



## vertical-align

+ **인라인 요소의 수직 정렬** 속성
+ **인라인 레벨 요소 또는 테이블 셀 상자의 수직 정렬**을 지정함.
+ block 요소가 아닌 **inline또는 inline-block에서만 사용** 가능

```css
vertical-align: keyword | length | percent | initial | inherit ;
```

+ 속성값 (inline elements에서)
  + **default : baseline**
  + **length** : 부모의 baseline에서 요소의 baseline을 주어진 길이 만큼 올리거나 내림. 음수 값 사용 가능 (0px === baseline)
  + **% percent** : 부모의 baseline에서 요소의 baseline을 line-height를 기준으로 % 값을 적용한 값만큼 올리거나 내림. 음수 값 사용 가능.
  + keyword
    + **baseline** : 기본 값. 소문자 x 기준 하단 라인
    + **sub** : 요소의 baseline을 부모 아래 첨자 basline으로 정렬
    + **super** : 요소의 baseline을 부모 위 첨자 basline으로 기준 정렬
    + **text-top** : 요소의 top을 부모 텍스트의 top으로 정렬
    + **text-bottom** : 요소의 bottom을 부모 텍스트의 bottom으로 정렬
    + **middle** : 요소의 middle을 부모 baseline + 소문자 x의 height / 2 에 정렬
    + **top** : 라인에서 가장 높은 요소의 top을 기준으로 정렬
    + **bottom** : 라인에서 가장 낮은 요소를 기준으로 정렬





## text-align

+ 내부 **인라인 요소의 수평 정렬을 지정**하는 속성

```CSS
text-align: left | right | center | justify | initial | inherit ;
```

+ 속성값
  + **default : left (문서의 방향과 언어에 따라 달라질 수 있음. right to left 언어는 default가 right)**
  + **start** : default 값
  + **end** : default 반대 방향
  + **left** : 텍스트를 왼쪽으로 정렬
  + **right** : 텍스트를 오른쪽으로 정렬
  + **center** :  텍스트를 가운데 정렬
  + **justify** : 텍스트를 좌우 라인 양쪽으로 붙여서 정렬. 마지막 라인은 정렬 안 함.





> ### 💡 요소들의 수평 중앙 정렬
>
> + text-align은 block 요소에 해당 속성을 지정하여, 속성을 지정한 요소 자체가 아닌 그 내부의 inline-level을 정렬함.
>
>   block 요소 자체를 가운데 정렬하려면, margin을 사용한다
>
>   → **inline 요소는 부모 요소에 `text-align: center` 를 선언**하여 수평 중앙 정렬
>
>   ​	**block 요소는 자기 자신에 `margin: 0 auto` 를 선언**하여 수평 중앙 정렬

