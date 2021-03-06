# 항해 99 (스파르타 코딩 클럽) 6주차 회고록

이번주에는 클론코딩을 마무리하고 새로운 미니프로젝트를 위한 준비를 했다.<br>
리덕스를 좀 더 편하게 사용할 방법을 찾아보았다.

## [Clone_Coding (인스타그램)](https://github.com/DabinLim/Clone_coding)

드디어 클론코딩이 끝났다.<br>
처음 시작할땐 파이어베이스로 밖에 프로젝트를 안해봤기 때문에 서버와 api를 이용해서 데이터를 주고 받는 게 굉장히 헷갈렸다.<br>
하지만 고생끝에 첫 연동에 성공한 이후로는 속도가 붙어 언제 그랬냐는 듯 프로젝트를 진행해 나갔다.<br>
서버에서 받은 데이터를 관리해서 필요한 곳에 뿌려주고 리덕스 상태관리 하고 <br>
계속해서 반복하다 보니 이제는 확실히 감이 잡힌 것 같다.<br>
저번주에 리액트 심화과정이 끝났을때는 강의 내용의 30-40%정도 밖에 이해하지 못한거 같았는데 이제는 80-90%정도는 이해가 된 것 같다.<br>
같은 팀의 프론트분과 다른 팀의 프론트 분들을 도와드릴때마다 더 깊게 이해하게 되는 것 같다.<br>
항해를 하면서 가장 큰 폭의 성장을 한 일주일이라고 생각이 든다.

## 미니 프로젝트 셋팅

클론코딩이 끝난 후 새로운 팀이 만들어졌다.<br>
이번엔 spring3명, react 2명이 팀이 되었다.<br>
실시간 채팅 어플을 만들기로 기획하였는데 아직 양방향 통신에 대해 이해가 부족한것 같아 파이어 베이스의 real time 데이터베이스를 이용해 연습을 했다.<br><br>
리액트에도 부트스트랩이 있길래 사용해봤는데 음.. 필요한 부분만 가져다 쓰면 괜찮을 것 같기도 하다<br><br>

그리고 로그인 로그아웃 레이아웃을 만들어놓고 리덕스를 사용하기 위해 configStore 를 작성해 놓은 후 프론트 팀원분께 말씀 드렸더니 Redux-toolkit을 사용해볼 생각이 없냐고 하셨다.<br>
안그래도 리덕스를 사용하면서 뭐 하나 하려면 너무 많은 코드를 써야 되는 것이 불편했는데 Redux-toolkit을 검색해보니 코드도 많이 줄어들고 편하게 사용할 수 있을 거 같아서 오늘 하루는 사용법을 공부하였다.<br><br>
공식문서도 찾아보고 구글링도 해봤는데 나는 왜 이렇게 헷갈리는지 모르겠다.<br>
[redux-toolkit](https://www.youtube.com/watch?v=2eTmICvKilA)<br>
결정적으로 위의 유튜브에서 도움을 받아 결국은 해냈다.<br>
자동자막이라 자막이 좀 엉망이긴 하지만 이제는 어느정도 익숙해진 리액트에서 쓰이는 용어들 + 주입식 영어교육의 결과물 + 엉망이지만 한두개씩은 들어오는 단어들을 조합하여 듣다보니 어떻게 사용해야 할지 감이 오기 시작했다.<br>

아직 이해가 안가는 부분도 있지만 일단은 사용이 가능하게 configStore 셋팅을 하고 createSlice를 이용하여 reducer를 만든 후에 원하는 state에 입력한 정보가 잘 저장이 되는 것을 확인한 후 프론트 팀원분께 개인톡을 보내 말씀드렸다.<br>
코드가 1/3 정도로 줄어든것 같다. 굉장히 만족스러웠다.<br>
이것만 해도 된다고? 했는데 진짜 된다. 신기하다.<br>
저번주에는 axios를 사용하여 api연동을 하였는데 이번주에는 공부 삼아 fetch도 사용해보면 좋을 것 같다.<br>
이번에도 새로운 걸 많이 배울 수 있을 것 같다.<br>
끝


