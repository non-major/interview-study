# MVC와 MVVM 패턴의 차이를 설명해주세요.

## 답변

MVC패턴은 Model + View + Controller를 합친 용어입니다. MVC는 사용자의 액션이 컨트롤러에 들어오면, 컨트롤러가 액션을 확인하고 모델을 업데이트합니다. 컨트롤러는 모델을 나타내줄 view를 선택하고, view는 모델을 이용하여 화면을 나타냅니다.

MVVM 패턴은 Model + View + View Model을 합친 용어입니다. 뷰모델은 뷰를 나타내 주기 위한 모델이자 뷰를 나타내기 위해 데이터 처리를 하는 부분입니다. 액션이 뷰를 통해 들어오면, 뷰 모델에 액션을 전달하고, 뷰 모델은 모델에게 데이터를 요청하고, 모델은 요청받은 데이터를 뷰 모델에게 응답하고, 뷰 모델은 받은 데이터를 가공하여 저장합니다. 뷰는 뷰 모델과 데이터 바인딩을 하여 화면을 그리는 동작 방식입니다.

## MVC 패턴의 특징 및 장단점

   <img src='https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F7IE8f%2FbtqBRvw9sFF%2FAGLRdsOLuvNZ9okmGOlkx1%2Fimg.png' width='300'>

1. 특징  
   Controller는 여러개의 View를 선택할 수 있는 1:n 구조입니다.  
   Controller는 View를 선택할 뿐 직접 업데이트 하지 않습니다.
1. 장점  
   MVC 패턴의 장점은 널리 사용되고 있는 패턴이라는 점에 걸맞게 가장 단순합니다. 단순하다 보니 보편적으로 많이 사용되는 디자인패턴입니다.
1. 단점  
   MVC 패턴의 단점은 View와 Model 사이의 의존성이 높다는 것입니다. View와 Model의 높은 의존성은 어플리케이션이 커질 수록 복잡하지고 유지보수가 어렵게 만들 수 있습니다.

## MVVM 패턴의 특징 및 장단점

<img src='https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FCiXz0%2FbtqBQ1iMiVT%2FstaXr7UO95opKgXEU01EY0%2Fimg.png' width='300'>

1. 특징
   MVVM 패턴은 Command 패턴과 Data Binding 두 가지 패턴을 사용하여 구현되었습니다.  
   Command 패턴과 Data Binding을 이용하여 View와 View Model 사이의 의존성을 없앴습니다.  
   View Model과 View는 1:n 관계입니다.
2. 장점  
   MVVM 패턴은 View와 Model 사이의 의존성이 없습니다.  
    각각의 부분은 독립적이기 때문에 모듈화 하여 개발할 수 있습니다.
3. 단점
   MVVM 패턴의 단점은 View Model의 설계가 쉽지 않다는 점입니다.

참고 : https://beomy.tistory.com/43
