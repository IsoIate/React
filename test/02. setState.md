## setState

- state의 값을 바꾸기 위한 함수
- 객체로 전달되는 값만 업데이트 함

```
state = {
  number : 0
  foo : 'bar'
}

this.setState{( number : 1 }) -> number의 값만 1로 변경, foo는 그대로
```

```
state = {
  number : 0
  foo : {
    bar : 0
    foober : 1
  }
}

this.setState ({
  foo: {
    foober : 2
  }
})  -> foober의 값이 변경되지 않고 foo의 객체가 바뀌어버림
```

- 위와 같은 상황일 때에는 아래와 같이 실행해야 함

```
this.setState({
  number: 0,
  foo: {
    ...this.state.foo,
    foobar: 2
  }
});
```

### setState에 객체 대신 함수 전달

```
// 기존 방식, this.state를 또 조회해야 함
this.setState({
  number: this.state.number + 1
});

// 변환 방식
this.setState(
  (state) => ({
    number: state.number
  })
);

// 비구조화 할당 사용
this.setState(
  ({ number }) => ({
    number: number + 1
  })
);
```













