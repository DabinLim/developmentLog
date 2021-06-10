# React를 사용하는 이유

## 리액트의 장점

### SPA, CSR 

서버로부터 데이터를 받아서 클라이언트에서 렌더링 하는 방식이다.<br>
서버로부터 데이터를 받아 바뀐 부분의 데이터가 있는 화면만 새롭게 렌더링하여 사용자 경험을 높여준다.<br>
또 서버가 렌더링하는 대신 데이터만 보내주는 경우 안드로이드, ios, 웹 모바일 등 다양한 플랫폼이 서버를 공유할 수 있게 된다.<br>
**CSR은 검색엔진 SEO를 최적화 할 수 없는 문제가 있는데 리액트에서는 CSR 과 SSR를 함께 사용할 수 있다.**

### 컴포넌트 기반의 화면 구성

리액트는 화면의 한 부분을 컴포넌트 단위로 나눌 수 있으며 독립적으로 관리 할 수 있다.<br>
컴포넌트는 역할과 기능에 따라 따로 관리하기 용이하며, 코드 재사용성을 높여준다.<br>

### 가상 DOM으로 인한 빠른 속도

> Virtual DOM 이란 UI의 이상적인 표현을 메모리에 저장하고 ReactDOM 과 같은 라이브러리에 의해 실제 DOM과 동기화하는 프로그래밍 개념이다, 이 과정을 재조정이라고 한다.

<br>
기존에는 DOM을 조작해서 브라우저에 화면을 나타내는 형식이었다. DOM 자체의 성능은 느리지 않지만 매번 DOM 전체에 직접 접근하여 변화를 주변 느려질 수 밖에 없다.<br>
리액트에서는 가상 DOM을 이용해 실제 DOM을 조작하는 횟수를 줄여 성능을 빠르게 개선하였다.<br>
데이터가 변경되면 리액트는 가상 DOM를 다시 변경한다. 그리고 이전의 가상 DOM과 비교해서 변경된 부분을 체크하고 변경된 부분만 실제 DOM에 적용한다.<br>
DOM을 매번 리렌더링 했던 기존 방식에 비해 빠르며, 규모가 클수록, 데이터의 변경이 많을수록 더 큰 힘을 발휘한다.