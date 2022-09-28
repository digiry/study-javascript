# 자바 스크립트 고급

## this 키워드

html 에선 글로벌 객체는 window 임.

따라서 최상위에서 사용한 `this`는 window 객체를 나타낸다.

```html
<script>
    console.log(this);
</script>
```

## scope

scope는 변수 접근성을 의미한다.

javascript `function`으로 선언한 부분을 html을 읽어서 해석할 때 html 내 모든 fuction을 load 한다.

하지만 변수에 함수를 할당한 경우에 해당 함수를 호출하는 경우 함수 정의보다 아래에 위치해야 한다.

## default parameter

ES6 (Ecmascript 6 버전)에 추가된 기능임
