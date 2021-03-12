## null
- 식별되지 않은 상태이며 어떠한 객체도 가지고 있지 않음
- 어떤 값이 의도적으로 비어있음을 명시
```
var a = null;
typeof(a) -> object
```

## undifined
- 변수에 값을 할당하지 않은 상태 또는 변수 자체가 없는 상태
- 쓰레기 값 대체?
- 예약어가 아니기때문에 변수명으로 사용할 수는 있으나 유지보수 측면에서 비추천
- null과 undefined는 동등하지만 일치하지는 않음
- 
```
if(null == undefined) -> true
if(null === undefined) -> false
```

```
function test(t) {
  if (t === undefined) {
    return 'Undefined value!';
  }
  return t;
}

let x;

console.log(test(x));
// expected output: "Undefined value!"
```

## 적용사례
- undefined는 값이 없는 것
- null은 하나의 타입이자 값

```
let logHi = (str = 'Hi') => {
  console.log(str);
}

logHi(undefined) -> Hi

let logHi = (str = 'Hi') => {
  console.log(str);
}

logHi(null) -> null
```
- undefined는 값이 없으므로 logHi함수에 넣어도 출력이 되지만 null은 하나의 타입이자 값이므로 null을 출력하게 된다
