# 이벤트루프란 무엇인지 설명해주세요

## 답변

싱글 스레드 기반의 언어인 자바스크립트는 이벤트 루프를 이용해서 비동기 방식으로 동시성을 지원합니다. 이벤트 루프는 콜 스택과 콜백 큐의 상태를 체크하여, 콜 스택이 빈 상태가 되면 콜백 큐의 첫번째 콜백을 콜 스택으로 밀어주는 역할을 합니다.

<img src='https://baeharam.netlify.app/media/js/overview.png' width='700' >

## 콜 스택이란?

코드가 실행되는 순서는 호출 스택에 의해 처리됩니다. 다음에 실행할 항목에 대한 명령 목록을 보유하는 배열로 생각할 수 있습니다.

## Web API란?

JavaScript 엔진의 일부가 아닌 모든 것은 별도의 스레드에서 처리됩니다. setTimeout 또는 Promise와 같이 브라우저에서 얻을 수 있는 다양한 기능을 말합니다.

## 콜백 큐란?

setTimeout이나 setInterval과 같은 비동기 함수의 콜백 함수 또는 이벤트 핸들러가 일시적으로 보관되는 영역입니다.

## (참고) 마이크로 태스크 큐란?

위 그림에는 없지만 ES6에서 새롭게 도입된 개념인 마이크로 태스크 큐(microtask queue)도 존재합니다. 잡큐(job queue)라고도 불립니다.  
마이크로 태스크큐는 이벤트 루프 대기열의 맨 위에 있는 레이어입니다. 이 큐에는 프로미스의 후속 처리 메서드의 콜백 함수가 일시 저장됩니다.  
프라미스 객체의 .then, .catch, .finally 콜백 함수가 보관되는 영역이라고 보면 됩니다.  
콜백 함수나 이벤트 핸들러를 일시 저장한다는 점에서 태스크 큐(콜백 큐)와 동일하지만, 마이크로 태스크 큐는 태스크 큐보다 우선순위가 높습니다.  
즉 이벤트 루프는 호출 스택이 비면, 먼저 마이크로 태스크큐에서 대기하고 있는 함수를 가져와 실행하고, 이후 태스크 큐에서 대기하고 있는 함수를 가져와 실행합니다.

참고 사이트  
https://baeharam.netlify.app/posts/javascript/event-loop  
https://www.webtips.dev/webtips/javascript-interview/what-is-the-event-loop  
https://ajdkfl6445.gitbook.io/study/web/event-loop
