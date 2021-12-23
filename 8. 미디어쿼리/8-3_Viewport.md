# Viewport

+ **웹 페이지에서 사용자가 볼 수 있는 영역**
+ 사용자 기기의 스크린 사이즈가 아닌, **브라우저의 가상 화면 사이즈**



### viewport 설정

+ viewport는 `<meta>` 태그에서 설정되고, 이는 `<head>` 태그에 위치한다.
+ name 속성에 "viewport"라고 선언하고, content 속성에 설정 내용이 들어간다.

```html
<meta name="viewport" content="뷰포트의 설정 값" >

<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

+ content에는 다음과 같은 내용을 설정할 수 있다.
  + **width** 또는 **height** :  뷰포트의 가로 또는 세로 크기를 지정. 대부분 특수 키워드 "device-width" 또는 "device-height"를 사용하며 이는  기기의 스크린 width 또는 height 크기로 설정한다는 의미. px 단위의 수치도 들어갈 수는 있음.
  + **initial-scale** : 페이지가 처음 나타날 때 초기 줌 레벨 값을 설정. (소수 값)
  + **user-scalable** : 사용자의 확대/축소 기능 설정



> #### 💡 viewport 설정이 필요한 이유?
>
> 스마트폰 이전에는 대부분의 웹 페이지가 데스크탑 모니터 사이즈를 기준으로 제작됨
>
> → 작은 화면에서는좌우 스크롤 해야 확인 가능함
>
> → 모바일 브라우저에서 viewport라는 가상의 화면을 만들고 거기에 페이지를 나타내기 시작함.
>
> → 작은 화면인 모바일 기기에서 웹 페이지 전체를 표시하려니, 전체 페이지가 축소되며 글자와 그림도 함께 작아져 가독성이 매우 떨어지는 문제가 생김
>
> → viewport의 크기와 스케일 조정이 필요함.

