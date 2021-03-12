## props
- 부모 컴포넌트에서 자식 컴포넌트에게 전달해주는 데이터 값 (읽기 전용)
- 자식은 받기만 하고 props 값을 수정할 수 없음

```
// MyName.js
import React, { Component } from 'react';

class MyName extends Component {
  render() {
    return (
      <div>
        안녕하세요! 제 이름은 <b>{this.props.name}</b> 입니다.
      </div>
    );
  }
}

export default MyName;

// App.js
import React, { Component } from 'react';
import MyName from './MyName';

class App extends Component {
  render() {
    return (
      <MyName name="리액트" />
    );
  }
}

export default App;
```

- deefaultProps를 사용해 기본값 설정 가능

```
// 클래스 내부 작성
static defaultProps = {
  name: '기본이름'
}

또는
// 클래스 외부 작성
MyName.defaultProps = {
  name: '기본이름'
};
```

## state
- 컴포넌트 내부에서 선언하며 값 변경 가능
- 값 변경 시 setState 사용
