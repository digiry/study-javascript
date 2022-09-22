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
