## Selector
HTML 의 어떤 태그를 선택할 것인가를 규정 하는 문법

## 기본 선택자
- 전체 선택자 : 모든 요소
- 타입 선택자 : html 태그 타입이 일치하는 모든 요소
- 클래스 선택자 : 주어진 class 특성을 가진 모든 요소
- ID 선택자 : 주어진 id 특성을 가진 모든 요소(단, id 는 unique 할 것을 권장)
- 특성 선택자 : 주어진 특성을 가진 모든 요소를 선택

```html
<style>
    /* 전체 선택자 */
    * {

    }

    /* 타입 선택자 : tag */
    div {

    }

    /* 클래스 선택자 : .class */
    .class_name {

    }

    /* ID 선택자 : #id */
    #id {

    }

    /* 특성 선택자 : [] */
    [attribute_name] {
        /* attribute_name 의 속성을 갖는 요소 */
    }

    [attribute_name^=value] {
        /* attribute_name 의 속성값이 value 로 시작하는 요소 */
    }

    [attribute_name$=value] {
        /* attribute_name 의 속성값이 value 로 끝나는 요소 */
    }
</style>
```
<br>

## 그룹 선택자
- 선택자 목록(,) : 모든 일치하는 노드를 선택
```html
<style>
    div, span {
        /*모든 div 와 span 태그를 의미*/
    }
</style>
```
<br>

## 결합자
- 자손 결합자 : 첫 번째 요소의 자손인 요소
- 자식 결합자 : 첫 번째 요소의 바로 아래 자식인 요소
- 일반 형제 결합자 : 첫 번째 요소를 뒤따르면서 같은 부모를 공유하는 두 번째 요소
- 인접 형제 결합자 : 첫 번째 요소 바로 뒤에 위치하면서 같은 부모를 공유하는 두 번째 요소

```html
<style>
    A B {
        /*A 의 자손인 모든 B*/
    }

    A > B {
        /* A의 바로 아래 자식인 모든 B */
    }

    A ~ B {
        /* A 를 뒤따르는 모든 B (형제)*/
    }

    A + B {
        /* A 바로 뒤에 위치하는 모든 B (형제)*/
    }
</style>
```