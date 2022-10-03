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

## arrow function

익명함수에서 `function` 키워드를 삭제하고 `=>` 기호를 중간에 넣는다. 익명함수, arrow 함수도 마찬가지로 함수를 선언할 뿐이다.

호출하는 코드가 있어야 함수가 실행된다.

## Template literal

문자열 포맷팅하는 구문이다. 문자열 처리 구문을 간략하게 만들 수 있음

## spread operator

python `*args` 처럼 배열 요소를 나열하는 연산자다.


## object destructuring

object를 확장하고 특정 key만 지정하여 값을 노출하는 방법이다. React 코드에서 많이 본 코드 문법이다.

```javascript
function getPerson() {
    return {
    firstName: "John",
    lastName: "Doe",
    age: 37,
    email: "john@gmail.com",
    city: "New York",
    country: "USA",
    };
}

var person = getPerson();
console.log(person);

var {firstName, lastName} = getPerson();
console.log(firstName);
console.log(lastName);
```

## promise

javascript 코드에서 순차적으로 읽어 나가지만 문장 수행을 완료할때까지 기다리지 않고 다음코드를 처리한다. 비동기로 처리함. 어떤 구문이 외부 시스템에서 자원에 접근하는 처리라면 결과를 받기 전에 다음 코드가 처리되어 데이터를 받지 못한다.

예전에는 sleep 등을 사용하여 데이터를 받을 시간을 벌었지만 이제는 promise 객체를 사용한다.

비동기로 수행한 결과를 받을 수 있게 약속한다라는 의미같다.