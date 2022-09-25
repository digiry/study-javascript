# String 내장함수

python str처럼 public method가 많다. 실제 업무에서 string은 많이 사용하니 익숙해지도록 여러 함수를 눈에 익혀두자.

# Array 내장 함수

**shift**

shift 함수는 bit 조작에서 `<<` 와 비슷한 기능이다

```javascript
var poped = fruits.shift();
console.log(poped);

fruits.unshift("Lemon");
console.log(fruits);
```

**splice**

splice() 함수는 영어 단어 의미처럼 꼬아 잇는 동작을 한다. 배열 요소에서 지정한 위치에 넣기도 하고 넣기 전에 몇 개 요소를 삭제하고 넣기도 한다.

```javascript
var fruits = ["Banana", "Orange", "Apple"];
fruits.splice(1,0,"Lemon", "Kiwi");
console.log(fruits);
```

**sort**

sort() 함수가 매개변수를 기본으로 스트링으로 변환하는 걸 주의하자.

```javascript
var fruits = ["Banana", "Orange", "Apple"];
console.log(fruits.sort());

var points = [40, 100, 70, 21, 99];
console.log(points.sort());

points.sort(function(a,b) {
    return b - a;
})
console.log(points);

var persons = [
    {name:"유재석", point:78},
    {name:"김종국", point:92},
    {name:"양세찬", point:76},
    {name:"하하", point:81},
];

persons.sort(function(a, b) {
    return a.point - b.point;
});
console.log(persons);
```

**filter**

```javascript
var pass = persons.filter(function(person) {
    return person.point > 80;
});
console.log(pass);
```

**reduce**

매개변수 정의

* a (accumulator): 누산기
* c (currentValue): 배열을 읽으면서 현재값
* i (currentIndex): 현재 읽고 있는 배열 index 값
* arr (currentgArray): 값이 누적된 전체 배열

```javascript
var total = arr1.reduce(function(a, c) {
    return a + c;
});
console.log(total);
```

**map**

```javascript
var userList = [
    {firstName: "재석", lastName: "유", email: "yu@gmail.com"},
    {firstName: "종국", lastName: "김", email: "kim@gmail.com"},
    {firstName: "세찬", lastName: "양", email: "yang@gmail.com"},
    {firstName: "석진", lastName: "지", email: "ji@gmail.com"},
];

var userList2 = userList.map(function(user) {
    return {fullName:user.lastName + user.firstName, firstName: user.firstName, lastName: user.lastName };
});
console.log(userList2);
```

## Date

왜 javascript Date()에서 month는 0-based인가?

Java와 C에서의 time.h 에서 넘어온 유물이다.

월표시를 숫자로도 하지만 월 이름 축약도 많이 써서 배열에 담고 사용하기 편하기 위해 12개 배열을 사용해서 이다.

* https://stackoverflow.com/questions/2552483/why-does-the-month-argument-range-from-0-to-11-in-javascripts-date-constructor

* https://stackoverflow.com/questions/31380566/why-does-tm-mday-start-from-1-while-all-other-elements-of-struct-tm-start-from-0

내장 Date보다 업계에서는 `moment.js` 라이브러리를 많이 사용한다.

## Math

**floor**

소수부를 내리는 함수로 음수이면 소수를 포함한 음수에서 내리면 더 작은 음수가 됨.

```javascript
console.log(Math.floor(9.9));
console.log(Math.floor(-4.2));
```

**trunc**

단순하게 정수부만 남김

```javascript
console.log(Math.trunc(9.9));
console.log(Math.trunc(-4.2));
```

## Json

json 형태로 직렬화, 역직렬화가 편하다

```javascript
var data = {
    "employees": [
    {"firstName":"John", "lastName":"Doe"},
    {"firstName":"John2", "lastName":"Doe2"},
    {"firstName":"John3", "lastName":"Doe3"},
    ]
};

console.log(data);

console.log(JSON.stringify(data));

var text = '{"employees":[{"firstName":"John","lastName":"Doe"},{"firstName":"John2","lastName":"Doe2"},{"firstName":"John3","lastName":"Doe3"}]}';

var data2 = JSON.parse(text);
console.log(data2);
```