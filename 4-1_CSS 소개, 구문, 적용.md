# CSS



## CSS (Cascading Style Sheets)

+ Mark-Up 언어를 꾸며주는, 표현을 위한 언어
+ HTML 문서를 디자인하는 역할
+ HTML이 웹페이지의 정보를 표현한다면, CSS는 HTML을 디자인하는 역할을 한다. CSS는 표현할 대상인 마크업 언어 HTML과 묶어서 이야기한다.



## CSS 문법

### CSS 구문

```css
h1 { color: yello; font-size: 2em; }
```

+ 선택자(selector) - "h1"
+ 속성(property) - "color", "font-size"
+ 값(value) - "yello", -"2em"
+ 선언(declaration) - "color: yellow", "font-size: 2em"
+ 선언부(declaration block) - "{ color: yello; font-size: 2em; }"
+ 규칙(rule set) - "h1 { color: yello; font-size: 2em; }"



+ 속성 이름과 속성 값 사이 개행하지 말 것. 선언과 선언 사이에는 개행 가능.
+ HTML의 속성은 attribute, CSS의 속성은 property



### 주석

```css
/* 주석 내용 */

/* 주석은
	여러 줄로
	작성 가능 */
```



### CSS 적용방식

+ inline

  ```HTML
  <div styles= ... >  내용 </div>
  ```

  + 스타일을 적용할 요소에, 직접 스타일 속성을 이용하여 규칙을 선언. 선언부 내용만 스타일 속성 값으로 줌.

  + 스타일 코드의 재활용이 되지 않아 자주 사용 안 함.

    

+ internal

  ``` CSS
  <style> ... </style>
  ```

  + `<style>`을 이용하는 방식. 

  + `<head>` 내부에 ` <style>`, 그 내부에 스타일 규칙을 작성함.

  + **각 페이지마다 스타일 규칙을 선언**하는 방식으로, **페이지가 많고 스타일 규칙이 많아지면 한계**가 생김.

    

  + ```css
    <style> div { color: red; } </style>
    ```

    위와 같이 작성하면, 모든 `<div>`에 선언한 스타일 적용됨.

    

+ External

  ``` CSS
  <link rel="stylesheet" href="css/style.css">
  ```

  + **외부 스타일 시트** 파일을 이용하는 방법. 

  + 스타일 규칙을 별도의 외부 파일에 선언하는 방식으로, 해당 외부 파일의 확장자는 `.css`로, CSS 파일이라고 부름

  + 여러 페이지에 하나의 외부 스타일 시트를 사용하면, 모든 페이지에 같은 스타일을 적용할 수 있음. 수정이 필요할 때도 CSS 파일만 수정하면 연결된 모든 페이지에 반영됨.

  + 파일 관리가 편하고 용량이 작아 주로 사용되는 방식.

    

  1. CSS 파일에 스타일 규칙을 선언하여 저장함.
  2. `<head>` 내부에 `<link>`를 선언하고, rel 속성에는 'stylesheet', href 속성에는 적용할 CSS 파일의 경로를 작성함.
     + rel 속성은 문서와 연결 파일의 관계를 명시하는 속성. CSS는 'stylesheet'라고 작성

  

+ @import

  ```CSS
  @import url("css/style.css");
  ```

  + 스타일 시트 내에서 다른 스타일 시트 파일을 불러오는 방식
  + `<style>` 내부 상단 또는 외부 스파일 시트 파일 상단에 선언
  + 성능이 좋지 않아 거의 쓰이지 않음

