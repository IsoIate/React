## IIFE
- IIFE 란 정의와 동시에 즉시 실행되는 함수를 의미
- 즉시 실행 함수는 함수 리터럴을 () 로 감싼 뒤 바로 실행하는 형태가 일반적입니다

```
(function () { console.log('Hello World') })(); // Hello World
```

### 함수 리터럴 (Function Literal)
- 자바스크립트에서 함수를 정의하는 표현식을 "함수 리터럴" 이라고 함
- 함수 리터럴은 아래 4개의 요소로 구성

  - 예약어 function (필수)
  - 함수이름 (선택)
  - 매개변수 집합 (필수)
  - 함수 본문 (필수)
```
function add(a, b) {
  return a + b
}
```
- 아래처럼 이름 없는 함수로 작성하면 에러 발생

```
function (a, b) { return a + b } // Uncaught SyntaxError: Unexpected token (
```
- 함수 이름 없이 정의하는 경우에는 아래 조건이 충족되어야 함
  - 이 함수를 할당 받을 변수를 지정
  - 이 함수를 즉시 호출
  
```
const add = function (a, b) { return a + b };
(function(a, b) { return a + b })(1, 2); // 3
```

#### IIFE - 익명 함수 표현식 (즉시 호출 함수)
```
(function () {
  if (value === 1) return  (<div>하나</div>)
  if (value === 2) return  (<div>둘</div>)
  if (value === 3) return  (<div>셋</div>)
})()    
```

#### 화살표 함수 (람다?)
```
(() => {   
  if (value === 1) return  (<div>하나</div>)
  if (value === 2) return  (<div>둘</div>)
  if (value === 3) return  (<div>셋</div>)
}) ()
```
