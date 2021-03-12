## Equals의 종류

### Double Equals (==)
- loose equality (느슨함)
- 비교 이전에 타입 변환을 하고 비교를 함
- String A, Number B일 때 A == B를 하면 타입 변환을 하고 비교를 함

```
console.log(77 == "77") -> true
```

### Triple Equal(===)
- strict equality (엄격함)
- 비교할 때 타입 변환이 발생하지 않음
- 값이 같은지, 타입이 같은지 판별하여 비교

```
console.log(77 = "77") -> false
```
