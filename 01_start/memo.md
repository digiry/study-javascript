# 메모

## 자바스크립트 작성 위치

javascript 코드는 html 파일에서 head, body 태크 내에 정의할 수 있다.

javascript 코드는 script 태그 안에 구현할 수 있다.

js 파일로 분리할 수 있다.

js 를 불어오는 코드를 body 맨 아래에 두어야 웹페이지 로딩할 때 js 파일을 읽는 시간 때문에 화면이 늦게 그려지는 걸 막을 수 있다.

## 변수 선언

var 키워드로 변수 선언은 중복된 변수명으로 선언이 가능하다.

> var 키워드가 다른 언어와 다른 변수 선언 문법이다. 중복으로 선언을 지원하는 이유는 뭘까? javascript에서 legacy를 호환하기 위해서 일꺼 같다.

let 키워드로 변수 선언은 중복 선언을 할 수 없다.

> 재선언하면 SyntaxError 발생


const 키워드는 상수 선언이다.

> const 변수에 값 변경하면 TypeError가 발생한다.

## 데이터 타입

undefined 는 하나의 데이터 타입으로 평가한다.

```javascript
>>> let u;
>>> console.log(u);
undefined
```

## 부동 소수점

Javascript는 실수를 64비트 부동소수점으로 저장한다.

큰 실수를 다룰때 BigNumber.js, Big.js, Deciaml.js 라이브러리를 쓰는게 좋다.

## 연산자

문자열과 숫자를 연산하면 숫자를 문자열로 타입cast를 하고 문자열로 계산한다.

```javascript
    // 숫자와 문자 연산
    var x = 5 + 5;
    var y = "5" + 5;
    console.log(x);
    console.log(y);
```

```javascript
    // 비교 연산자
    console.log(1 == 1); # ==> true
    console.log(1 == "1"); # ==> true
    console.log(1 === "1"); # ==> false // 값과 data type까지 비교함
    console.log(1 != 3);
    console.log(1 != "1");
    console.log(1 !== "1");
```

## 반복문

for-in 구문이 배열 인덱스를 순회하는게 좀 이상하다.

객체가 가진 key를 for-in 가 나오게 한거 같다. 대신 for-of 구문이 객체 값을 읽는다.

```javascript
    // foreach
    var numbers = [42, 23, 5, 7];
    for (var idx in numbers) {
      console.log(numbers[idx]);
    }

    var person = {
      firstName: "John",
      lastName: "Doe",
      age: 30,
    };

    for (var key in person) {
      console.log(person[key]);
    }

    var numbers = [42, 23, 5, 7];
    for (var val of numbers) {
      console.log(val);
    }

```
