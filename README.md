# Web APIs 이해의 시작
 
## *APIs(Application Programming Interfaces)

### 개발자가 복잡한 기능을보다 쉽게 ​​만들 수 있도록 프로그래밍 언어로 제공되는 구성입니다. 더 복잡한 코드를 추상화하여 대신 사용하기 더 쉬운 구문을 제공합니다.



## *Web APIs

#### Web API collection : https://developer.mozilla.org/en-US/docs/Web/API




## *Browser 구조 분석
### window: 브라우저에서 현재 열려있는 전첵적인 창
### document: 페이지가 표시되는 부분




#### Window: https://developer.mozilla.org/en-US/docs/Web/API/Window
#### Document: https://developer.mozilla.org/en-US/docs/Web/API/Document
#### Viewport: https://developer.mozilla.org/en-US/docs/Glossary/layout_viewport
#### Navigator: https://developer.mozilla.org/en-US/docs/Web/API/Navigator




## *윈도우 사이즈 표기
### screen size: 모니터 사이즈
### outer size: 브라우저 전체 사이즈
### inner size: 웹페이지 수직 스크롤 포함 사이즈
### client size: 웹페이지 수직 스크롤 사이즈 제외 한 사이즈
```js
window.addEventListener('resize', () => {});

//screen
window.screen.width
window.scree.height

//outer
window.outerWidth
window.outerHeight

//inner
window.innerWidth
window.innerHeight
```



## *브라우저 좌표

```js
//요소의 너비와 높이 등 의 정보
Element.getBoundingClientRect()
```
### Client x, y
###### 브라우저 window의 x, y

### Page x, y
###### 문서의 제일 시작점 x, y



## *윈도우 스크롤링 APIs
#### scrollBy
#### scrollTO
#### scrollIntoView

```js
window.scrollBy();
window.scrollTO();
window.scrollIntoView();
```



## *Window load

```js
    //only document(HTML이 완료가 되면 호출)
    window.addEventListener('DOMContentLoaded', () => {
        console.log('DOMContentLoaded');
    });

    //after resources (css, images 등 모든 것들이 완료가 되면 호출)
    window.addEventListener('load', () => {
        console.log('load');
    });

    //before unload(사용자가 페이지를 나가기 전에)
    window.addEventListener('beforeunload', () => {
        console.log('beforeunload');
    });

    //resource is being unloaded
    window.addEventListener('unload', () => {
        console.log('unload');
    });
```
