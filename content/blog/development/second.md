---
title: 'Basic HTML'
date: 2021-06-25
category: 'HTML'
draft: false
---

# HTML,CSS

모든 웹사이트는 text로 이루어져 있다.  하지만 그 text 자체로는 우리가 시각적으로 보는 웹사이트를 만들 수 없다. 브라우저에게 text가 전달되었을 시에만 브라우저가 text를 이해하고 시각적으로 디스플레이 해주는 것이다. 따라서 브라우저가 이해하는 text는 HTML, CSS, Javascript뿐이다. 

HTML (Hyper Text Markup Language)

기능 = HTML은 content의 structure을 구성할 수 있는 유일한 언어. content중 어느 것이 title이고, sidebar이고, navigation이고, article인지 등을 브라우저에게 말해주는 언어임. 

CSS (Cascading Style Sheet) 

기능 = HTML의 content들에 디자인을 입혀줌. 글씨의 크기, 색깔, 이미지의 크기 등을 조절할 수 있음. 하지만, HTML이 없으면 꾸며줄 대상이 없기 때문에 홀로 사용할 수 없음. 반드시 HTML과 함께 쓰여야함.

HTML과 CSS

⇒ 둘 다 프로그래밍 언어로 분류되지 않음. Javascript만이 프로그래밍 언어로 분류됨.

- HTML = 뼈대, 단독으로 쓰일 수 있지만 content만 보여지게 되므로 디자인이 없음.
- CSS = 근육, 단독으로 쓰일 수 없음. 반드시 HTML과 같이 쓰여야함. HTML에 스타일을 더해줌.

Javascript

기능 = 웹페이지를 동적으로 만들어줌. interactivity가 추가됨. 인간의 뇌와 같은 역할을 함. javascript가 모든 웹사이트에 필요하지는 않음. 하지만 javascript를 쓰지 않은 웹페이지는 멍청하다...ㅎㅎ. 

---

### 주의사항

- 폴더명과 파일명은 항상 소문자로 쓰기
- 저장을 습관화 ⇒ 나의 경우 vscode 자동저장 설정 해놓음

### 환경세팅

- Extension : material theme (vscode theme), icon, wakatime (timetracker), prettier (formatting → cmd+s 누르면 저절로 save하면서 format 시켜줌)
- vs code 단축어
    1. 반복되는 단어 한방에 수정 : Cmd + D ⇒ 한번 누르면 같은 단어 하이라이트됨 (위치확인), 꾹 누르면 모두 선택됨
    2. 클릭하는 곳마다 커서 생성 : Alt + Click
    3. 해당 줄의 코드 위/아래로 움직이기 : Alt + ↑ / ↓
    4. 코드 복사해서 위/아래로 움직이기: Shift + Alt  + ↑ / ↓ 
    5. 코드 블록 한방에 코멘트 처리하기 : Cmd + / 
    6. 선택된 영역에 커서 만들기 : Shift + Alt  + i
    7. 마우스가 가는 곳 마다 커서 만들기 : Shift + Alt  + Mouse Drag
    8. 사이드바 숨기기 : Cmd + B 
    9. 코드의 맨앞/맨뒤로 이동: Cmd + ← / →

---

### HTML

— 확장자는 .html

— html파일은 browser에서 열어야 함.

Structure

- `<!DOCTYPE html>` : html5로 작성되었다는 것을 브라우저에게 전달하는 역할
- `<html></html>` : 이 안에 들어가는 내용이 html이라는 것을 알려주는 태그
    - lang : 웹사이트의 언어가 주로 어떤 것인지 명시해주는 부분.
- head : 보이지 않는 meta data들을 저장하는 부분 ⇒ title를 제외하고는 눈에 보이지 않음
    - title : 탭에 보여짐. 웹사이트의 이름을 의미하는 태그.
    - meta :  title, link, style를 제외한 부가적인 정보들을 저장할때 쓰이는 태그
        - name : name에서 부가적인 정보의 종류를 지정하고, content에서 정보 내용을 씀. content와 같이 쓰임.
            - name = description : 구글에서 검색할시 제목 아래 나오는 설명
        - property : name과 같이 부가적인 정보의 종류를 지정하고, content에서 정보 내용을 씀. content와 같이 쓰임.
            - property = og: -  : 링크를 공유할때 보여지는 title, url, image, description등을 제어할 수 있음
        - content : name 속성에서 지정한 것에 대한 실질적인 내용을 작성함.
        - charset : 문자를 렌더링하는 방식을 지정. 주로 utf-8를 사용. utf-8의 경우 다양한 나라의 언어를 지원해서 깨지는 현상이 발생하지 않음.
    - link :
        - rel : relation을 뜻하며, link와 html 파일간의 관계를 명시해줌
            - rel = 'stylesheet' href='주소' : css파일을 연결시켜주는 부분.
            - rel = 'shortcut icon' href='주소' : favicon을 설정하는 부분. 탭에서 title 옆에 보여짐
- body : 실제 눈여 보여지는 content들을 저장하는 부분

```jsx
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Rachel's Website</title>
    </head>
    <body>
        <h1>Hello</h1>
    </body>
</html>
```

debug

- 브라우저는 왠만하면 html에 오류가 있더라고 content를 보여주려고 함. 오류가 발생했는지 여부나 어디에서 오류가 발생했는지 보여주지 않음

tag

- content에는 tag를 붙여줌 → syntax : <tagName> content </tagName>
    - 반드시 opening tag와 closing tag가 있어야함. closing tag가 없으면 계속적으로 이어짐
    - 일회성 태그들은 closing tag가 없어도 됨 ⇒ ex. img
- tag들로 인해서 브라우저에게 content의 의미를 전달해줄 수 있음. tag가 없으면 브라우저는 content를 그냥 아무 의무없는 text로 받아들임

    ⇒ ex. h1~h6 태그 안에 content는 title이라는 것을 브라우저에게 전달하는 역할. 

- 절대 모든 태그의 종류들을 외울 필요는 없음. 외우는 것에 시간 낭비하지 말고 필요할 때 공식문서를 찾는 습관을 들일 것!

Semantic Tag

- 의미가 있는 태그들 : tag의 이름만으로 무슨 기능을 하는지 알 수 있는 태그들을 말함
    - header, main, footer, article, aside, nav 등
    - div와 동일한 박스, 컨테이너 역할을 하지만 의미가 있는 태그들. div를 쓰기보다는 semantic tag들을 쓰는 것이 좋음
- 의미가 없는 태그들 : div, span 등. 남발하는 것은 안좋음 ⇒ 가독성 떨어짐.
    - div의 경우 박스 역할을 함으로써 한 줄을 모두 차지하게 됨.
    - span은 짧은 text를 위한 태그, p는 paragraph를 위한 태그

attribute

- 모든 태그들에 다 쓰일 수 있는 공용 속성들이 있음 ⇒  ex. class, id
- 특정 태그들에만 쓰이는 속성들이 있음 ⇒ ex. src : img 태그에서만 쓰임 / href : a 태그에서 쓰임

    ( 이 속성들은 다른 태그들에 쓰였을 때 브라우저는 이해하지 못하므로 아무 변화가 없음 )

- 항상 value는 "" 안에 작성할 것. ( ` ` or ' '도 가능하지만 " "를 추천 )

List

- unordered list : `<ul></ul>` ⇒ default로 bullet point로 작성됨
- ordered lists : `<ol></ol>` ⇒ default로 1로 시작하는 숫자가 순서대로 앞에 쓰여짐.
- list items : `<li></li>` ⇒ 모든 list 안의 개별항목들을 li태그로 감싸줌

    ( li 태그로 감싸주지 않으면 개별적인 항목들이라고 브라우저가 인식하지 않음 )

Image

- self-closing tag: `<img src=" 주소 ">` ⇒ image는 안에 text가 존재하지 않고 image 자체가 content이기 때문에 closing tag가 존재하지 않음.
- attribute ⇒ src = source, image의 주소를 가져옴

Form

- 전체는 `<form></form>` 으로 감싸줌
- `<label></label>` : input과 같이 쓰임. Input을 설명하는 text.
    - for : label의 for과 input의 id가 서로 같은 값을 가져야 label과 Input이 연결됨. 연결되었을 때 label를 누르면 input이 저절로 실행되거나 선택됨.
- `<input />` : self-closing tag. form에서 여러 입력값들을 입력할 수 있는 박스가 생성
    - type
        - password : 비밀번호를 입력할 수 있는 form ( 입력하는 문자들이 점으로 보여짐 )
        - text : default값, 텍스트를 입력할 수 있는 form
        - submit : form을 제출할 수 있는 버튼 생성
        - file :  파일을 가져올 수 있음
            - accept : 확장자 제한 가능 ⇒  ex) .pdf , /image* (이미지 전체 확장자 = jpg, jpeg, svg, png ) 등..
    - 그외 attribute들
        - required : 필수 입력칸. 채우지 않으면 submit이 안되면서 오류 메세지 발생
        - placeholder = " ~ " : box에 내용을 입력하기전에 기본적으로 보여지는 글씨. 사용자가 입력하기 시작하면 사라짐
        - disabled : 입력할 수 없게 막아 놓는 기능
        - minlength : 최소 입력길이

ID

- id는 각 태그에 하나씩만 쓸 수 있으며 같은 이름의 id는 중복 사용이 불가하다.
- CSS를 이용해 선택을 할 때 id를 이용해서 선택할 수 있음

그외 다양한 태그들

- 절대 외우지 않을 것, 필요할 때마다 태그와 그것에 쓰이는 attribute들을 검색해서 사용할 것
- mdn을 항상 이용할 것 (w3school 비추)

- audio : 오디오를 추가하는 태그 ⇒ controls: 눈에 보여지게 함. autoplay: 자동재생. src : 파일주소
- pre : 미리 서식을 지정한 텍스트를 나타내며 요소 내 공백문자를 그대로 유지, 입력한 대로 내용을 보여줌 ⇒ code나 이모티콘을 쓸 때 사용됨.
- cite : 저작물의 출처를 표기할 때 사용함. 약간 기울어져서 보여짐
- code : 짧은 코드 조각을 나타내는 스타일을 사용해 자신의 콘텐츠를 표시. 자간이 동일한 스타일을 띔.
- abbr : 축약어에 대한 설명을 마우스를 올렸을 때 보여줌 ⇒ title 속성에 원하는 내용 적음
- mark : 현재 맥락에 관련이 깊거나 중요해 표시 또는 하이라이트한 부분을 나타냄
- strong : 중대하거나 긴급한 콘텐츠를 나타냅니다. 보통 브라우저는 굵은 글씨로 표시
- sub : 활자 배치를 아래 첨자로 해야 하는 인라인 텍스트를 지정
- sup : 활자 배치를 위 첨자로 해야 하는 인라인 텍스트를 지정 ⇒ 제곱근, 지수 표현할 때 주로 사용됨
