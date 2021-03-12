## LifeCycle API
- 컴포넌트가 브라우저에 나타날 때, 사라질 때, 업데이트 될 때 호출되는 API

### 컴포넌트 초기 생성
- 컴포넌트가 브라우저에 나타나기 전, 후에 호출되는 API

#### constructor
- 컴포넌트 생성자 함수
- 컴포넌트가 새로 만들어질 때마다 호출됨

```
constructor(props) {
  super(props);
}
```

#### componentDidMount
```
componentDidMount() {
  // 외부 라이브러리 연동: D3, masonry, etc
  // 컴포넌트에서 필요한 데이터 요청: Ajax, GraphQL, etc
  // DOM 에 관련된 작업: 스크롤 설정, 크기 읽어오기 등
}
```

### 컴포넌트 업데이트
- props 의 변화, 그리고 state 의 변화에 따라 결정됨
- 컴포넌트가 새로운 props 를 받게됐을 때 호출됨
```
componentWillReceiveProps(nextProps) {
  // this.props 는 아직 바뀌지 않은 상태
}
```


