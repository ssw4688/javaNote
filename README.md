## javaClass
220713 ~ 220823 <br>
국비 java 수업 자료 및 복습 내용



## 반복문

 * for문과 while문의 목적
   - for : 몇 번 반복할 지 알 때
   - while : 몇 번 반복할 지 모를 때


▷ do~while문 : 무조건 한 번은 실행 해야 할 때
   do{
      실행할 문장;
   }while(조건식);


## 기타 제어문
   break : 즉시 해당 중괄호 영역을 탈출한다.
      - if문 안에서 사용 시 if문을 탈출하지 않고 if문을 감싸고 있는 중괄호 영역을 탈출한다.

   continue : 즉시 다음 반복
      - 아래의 코드를 실행하지 않기 위해서 사용한다.
    


## 배열 : 저장공간의 나열
   1.
    변수를 여러 개 선언하면 이름도 여러 개 생긴다. 이 때 각 저장공간을 관리하기가 불편하다.
    따라서 n칸 배열을 한 번만 선언하면 저장공간도 n개 생기고, 이름도 한 개이기 때문에 관리하기 편하다.

   2.
    규칙성이 없는 값에 규칙성을 부여하기 위해서

배열의 선언

   자료형[] 배열명 = {값1, 값2, ...}; // 어떤 값을 넣을지 알 때 사용<br>
   자료형[] 배열명 = new 자료형[칸수]; // 어떤 값을 넣을지 모르나, 몇 칸 만들지는 알 때 사용<br>
   자료형[] 배열명 = null; // 어떤 값을 넣을지도 모르고, 몇 칸 만들지도 모를 때 사용한다.<br>
   배열명 = new 자료형[칸수];<br>

   ※ new : Heap 메모리에 할당, 초기값으로 자동 초기화<br>
   ※ null : 주소의 초기값, 어떤 주소를 넣을지 모를 때 작성하는 초기값<br>
   ※ 자바에서 배열은 항상 Heap(동적 메모리)에 할당되기 때문에 메모리 상, 동적배열만 존재한다.<br>

배열의 구조<br>
   int[] arData = {3, 5, 9, 6, 7};<br>

   arData라는 이름의 저장공간은 한 개 만들어지며, 여기에는 한 개의 값만 담을 수 있다.<br>
   5개의 값을 담기 위해서는 5칸이 필요하며, 이는 Heap에 할당된다. <br>
   5칸의 저장공간 중 첫번째 저장공간의 주소값이 arData 저장공간으로 들어가며, <br>
   다음 주소에 접근하기 위해서는 +n을 한다. 예를 들어, arData + 2는 9라는 값이 담긴 저장소의 주소값이 되며,<br>
   (arData + 2)는 해당 주소에 가서 읽어온 9라는 값이 된다. <br>
   JAVA에서는 직접 주소에 접근하는 연산자가 없기 때문에 위와 같은 식을 []로 치환하여 사용하며, arData[2]로 사용한다.<br>
   각각의 방 번호는 index라고 부르며, 배열은 시작주소를 가지고 있기 때문에 인덱스 번호는 항상 0부터 시작된다.<br>


length<br>
   배열을 선언하면 length라는 상수가 선언되고, 해당 배열의 길이가 담긴다.<br>
   배열명.length로 사용하게 된다.<br>


배열의 사용<br>
   int[] arData = new int[5]; // 저장공간<br>
   arData[0] = 10; // 저장공간<br>
   arData[0] + 9; // 값<br>
   System.out.println(arData); // 주소값<br>
   arData[2] = arData[0] + arData[1]; <br>
   System.out.println(arData[5]); // 오류<br>
  
  2차원 배열 : 배열 안에 배열<br>
   1차원 배열을 여러 개 선언할 때 관리하기 힘들기 때문에 2차원 배열을 한 번 선언한다.<br>

   ※ 2차원 이상의 배열은 메모리 낭비가 심하므로 선호하지 않는다.

2차원 배열<br>
   자료형[][] 배열명 = {{값1, 값2, 값3}, {값4,..}, ...};<br>
   자료형[][] 배열명 = new 자료형[행][열];<br>
   자료형[][] 배열명 = null;<br>
   배열명 = new 자료형[행][열];<br>

         □   arrData      arrData.length(행의 길이)<br>
        □□   arrData[행]   arrData[행].length(열의 길이)<br>
      □□□ □□□   arrData[행][열]<br>



## 메소드
   이름 뒤에 소괄호.<br>
   단, 키워드 뒤에 소괄호는 메소드가 아니다.<br>

   f   (x)   =   2x + 1<br>
   메소드   매개      리턴값<br>
   이름   변수<br>

메소드 선언<br>

   (1)리턴타입 (2)메소드명(자료형 (3)매개변수명, ...){<br>
      (4)실행할 문장;<br>
      (5)return 리턴값;<br>
   }<br>


   (1) 리턴 값이 있다면 리턴 값의 자료형을 작성하고, 리턴 값이 없다면 비워놓지 않고 void를 작성한다.<br>
   (2) 동사로 작성한다(연필(매개변수)을 쓴다(메소드)).<br>
   (3) 외부에서 전달받을 값이 있다면, 자료형과 순서에 맞게 선언해준다.<br>
       생략 시, 외부에서 값을 전달받을 수 없게 된다.<br>
   (4) 생략이 가능하며, 메소드의 기능을 구현하는 로직을 작성한다.<br>
   (5) 생략이 가능하다.<br>

메소드 선언 순서<br>
   문제) 두 정수의 덧셈 메소드 선언<br>

   1. 메소드의 이름을 생각한다.<br>
      sum, plus, add, getTotal, compute, ...<br>

      add(){}<br>

   2. 매개변수를 생각한다.<br>
      add(int num1, int num2){}<br>

   3. 실행할 문장을 생각한다.<br>
      add(int num1, int num2){<br>
         int result = num1 + num2;<br>
      }<br>

   4. 리턴 값을 생각한다.<br>
      add(int num1, int num2){<br>
         int result = num1 + num2;<br>
         return result;<br>
      }   <br>

   5. 리턴 타입을 결정한다.   <br>
      int add(int num1, int num2){<br>
         int result = num1 + num2;<br>
         return result;<br>
      }   <br>

메소드 주의사항<br>
   메소드를 선언할 때에는 {}중괄호가 있으며, 반드시 메소드 밖에서 선언한다.<br>
   메소드를 사용할 때에는 {}중괄호가 없으며, 반드시 메소드 안에서 사용한다.<br>

메소드 사용<br>
   메소드의 리턴 타입이 void면 실행 메소드이므로 값으로 봐서는 절대 안된다.<br>
   메소드의 리턴 타입이 void가 아니라면 사용한 부분 통채로가 리턴 값이다.<br>

메소드의 목적<br>
   1. 재사용(특정성을 부여해서는 안된다).<br>
   2. 소스코드 간결화<br>
   
리턴해야 할 때<br>
   사용한 쪽에 로직의 결과를 전달해야 할 때.<br>
   메소드 내에서 모든 작업이 끝날 수 없을 때.<br>

리턴하면 안될 때<br>
   사용한 쪽에 로직의 결과를 전달할 필요가 없을 때.<br>
   메소드 내에서 모든 작업이 완료될 때.<br>



## 클래스(반)
   공통요소를 한 번만 선언해 놓고 가져다 사용만 하도록 설계한다.

   1. 타입이다<br>
      클래스 안에 선언된 변수와 메소드를 사용하고 싶다면, 해당 클래스 타입으로 변수를 선언해야 한다.<br>
   2. 주어이다<br>
      Monkey.eat("바나나");<br>
      주어    동사  목적어<br>

클래스 선언<br>
   class 클래스명 {<br>
      필드(변수, 메소드)<br>
   }<br>

클래스의 필드 사용<br>
   1. 객체화(instance) : 객체(instance variable)를 만드는 작업, 추상적인 개념을 구체화시키는 작업.<br>
      클래스명 객체명 = new 생성자();<br>
      객체명.필드명<br>
      ※ .(마침표) : 하위 연산자, 멤버변수 접근 연산자, 닷 연산자, 점 연산자<br>
   2.static일 경우 클래스명으로 바로 접근 가능<br>

생성자
   클래스 이름 뒤에 소괄호가 있는 형태, 메소드와 기능이 똑같지만 메소드라고 부르지 않는다.<br>
   생성자는 리턴이라는 기능이 존재하지 않기 때문이다.<br>

   1. 해당 클래스의 필드를 메모리에 할당한 후 부여된 주소값을 가져온다.<br>
   2. 초기화<br>

기본 생성자<br>
   매개변수와 실행할 문장이 따로 없다.<br>
   클래스 선언 시, 자동으로 선언되며, 사용자가 직접 생성자를 선언하게 되면 기본 생성자는 없어진다.<br>

this<br>
   필드에 접근한 객체가 누구인지 알아야 해당 필드에 접근할 수 있다.<br>
   이 때 접근한 객체가 가지고 있는 필드의 주소값을 this라는 변수에 자동으로 담긴다.<br>

상속(inheritance)<br>
   1. 기존에 선언된 클래스의 필드를 새롭게 만들 클래스의 필드로 사용하고자 할 때<br>
   2. 여러 클래스 선언 시 필드가 겹치는 경우, 부모 클래스를 먼저 선언하고<br>
       공통 필드를 묶어서 자식 클래스들에게 상속해준다.<br>

상속 문법<br>
   class A{<br>
      A 필드<br>
   }<br>
   
   class B extends A{<br>
      A, B 필드<br>
   }<br>

A : 부모 클래스, 상위 클래스, 슈퍼 클래스, 기반 클래스<br>
B : 자식 클래스, 하위 클래스, 서브 클래스, 파생 클래스<br>

super() : 부모 생성자<br>
   자식 클래스 타입의 객체로 부모필드에 접근할 수 있다.<br>
   하지만 자식 생성자만 호출하기 때문에, 자식 필드만 메모리에 할당된다고 생각할 수 있다.<br>
   사실 자식 생성자에는 항상 부모 생성자를 호출하기 때문에 자식 생성자 호출 시 부모와 자식 필드 모두 메모리에 할당된다.<br>
   이 때 부모 생성자를 호출하는 방법은 super()를 사용하는 것이다.<br>
   만약, super()를 작성하지 않더라도 컴파일러가 자동으로 작성해준다.<br>


## 다형성(polymorphism)
   1. 오버로딩(중복정의)<br>
      매개변수의 개수 또는 타입이 다르면 동일한 이름의 메소드로 선언할 수 있다.<br>
   2. 오버라이딩(재정의)<br>
      부모 필드에서 선언한 메소드를 자식 필드에서 수정하고자 할 때 재정의를 해야 한다.<br>
      이는 자식에서 부모 필드의 메소드와 동일한 이름으로 선언하는 것이다.<br>
      부모 필드가 메모리에 먼저 할당되고 a라는 메소드가 먼저 올라간다고 하면,<br>
      자식 필드가 메모리에 할당되면서 재정의한 a메소드가 새롭게 만들어지는 것이 아니라<br>
      기존에 할당된 a메소드 저장공간에 새롭게 재정의한 자식 필드의 소스코드 주소가 들어가게 된다.<br>
      따라서 자식 객체로 a메소드에 접근하면 자식 필드에서 재정의한 소스코드의 내용이 읽히게 된다.<br>



## Storage class(저장 기억 부류)

   Stack      Data영역

   지역변수,매개변수   전역변수,정적변수(static)

초기화   직접      자동
생명주기   }      new, 프로그램 종료 시


   전역변수<br>
      생성자를 통해 메모리에 할당되며, 객체가 각각 가지고 있는 변수<br>

   static 변수(정적변수)<br>
      컴파일러를 통해 메모리에 1개 할당되며, 모든 객체가 공유하는 변수<br>



## 접근 권한 제어자(접근자)

   default : 다른 패키지에서 접근 불가 , 같은 패키지 접근 가능<br>
   public : 모든 곳에서 접근 가능, 해당 파일의 메인 클래스일 경우만 사용<br>
   protected : 다른 패키지에서 접근 불가, 자식은 가능<br>
   private : 다른 클래스에서 접근 불가, 메소드로만 접근하자!<br>


## Casting<br>
   up casting : 자식 값을 부모 타입으로 형변환<br>
   down casting : up casting된 객체를 자식 타입으로 형변환<br>
   ※ 부모 값을 자식 타입으로 형변환 시 오류<br>


Casting을 사용하는 이유<br>
   모든 자식 값을 전달받기 위해서는 동일한 타입의 저장공간으로 받아야 한다.<br>
   하지만 자식끼리는 서로 타입이 다르기 때문에 한 번에 전달받을 수가 없다.<br>
   이 때 up casting을 사용하면, 모든 자식이 부모 타입이므로 하나의 저장공간에 모든 자식을 받을 수 있게 된다.<br>
   만약 up casting으로 자식 값을 전달받았다면, 자식에서 새롭게 구현한 기능들은<br>
   사용할 수 없기 때문에 down casting을 통해서 복구하고 사용한다.<br>

- 객체 간 타입 비교(instanceof)<br>
   a instanceof A : 조건식, 참 또는 거짓 중 하나가 나오는 식<br>
   
   - a가 A타입이면 true<br>
   - a가 A타입이 아니면 false<br>


- 추상 클래스<br>
   - 필드 안에  구현이 안된 메소드가 선언되어 있는 클래스를 추상 클래스라고 한다.<br>
   이 때 구현되지 않은 메소드를 추상 메소드라고 부른다.<br>
   반드시 재정의를 통해 구현을 해야지만 메모리에 할당되기 때문에 "강제성"을 부여하기 위해서 추상 메소드로 선언한다.<br>

- 추상 클래스 선언<br>
   - abstract class 클래스명 {<br>
      abstract 리턴타입 메소드명(매개변수,...);<br>
      일반 메소드도 선언 가능<br>
   }<br>



- 인터페이스(interface) : 틀<br>
   - 추상 클래스를 고도화시킨 문법<br>
   상수와 추상메소드만 존재한다.<br>
   구현은 인터페이스를 지정한 클래스에서 진행하고,<br>
   인터페이스를 다른 클래스에 지정할 때에는 implements 키워드를 사용한다.<br>
   
  
  
- 추상 클래스와 인터페이스 간의 관계<br>
   - 인터페이스를 클래스에 바로 지정하면 모든 메소드에 강제성이 부여되어서<br>
   전부 다 구현해야 한다. 하지만 일반적인 상황에서는 모든 것이 아닌,<br>
   필요한 메소드를 골라서 재정의해야한다.<br>
   인터페이스를 직접 지정하지 않고 다른 클래스에 지정한 후 바디를 만들어 놓는다면,<br>
   강제성이 소멸되고 이 클래스를 상속받아서 필드를 구현한다면, 골라서 재정의할 수 있게 된다.<br>
   이 때 중간에서 강제성을 없애주는 클래스를 추상클래스로 선언하기로 하며,<br>
   추상 클래스 이름 뒤에는 Adapter를 붙여서 목적을 알려준다.<br>



- 마커 인터페이스(Marker Interface)<br>
   - 클래스들을 그룹화하기 위한 목적으로 사용한다.<br>
   인터페이스는 지정한 클래스의 부모이며, 모든 자식은 부모의 타입이므로<br>
   마커 인터페이스를 지정받은 클래스들이 하나의 타입으로 묶이게 된다.<br>
   이름 뒤에  Marker를 붙여줘야 한다.<br>



- 내부 클래스(Inner Class)<br>
   - 하나의 클래스에서 a작업과 b작업이 있을 때에는 따로 분리하여 클래스로 만들지 않고,<br>
   클래스 안에 클래스를 선언하여 설계한다. 이 때 밖에 있는 클래스를 외부 클래스라고 하며,<br>
   안에 선언된 클래스를 내부 클래스라고 한다. 외부 클래스가 메모리에 할당되어야<br>
   내부 클래스를 객체화할 수 있기 때문에 클래스를 숨기기 위해서 내부 클래스를 사용하기도 하며,<br>
   이를 캡슐화 또는 은닉화라고 한다. 내부 클래스는 외부 클래스의 필드이기 때문에<br>
   외부 클래스의 필드를 자신의 필드처럼 가져다 사용할 수 있게 된다.<br>
   ※ 메소드 안에서 클래스를 선언할 수도 있다.<br>

- 익명 클래스(Anonymous Inner Class)<br>
   - 이름이 없는 클래스이며 구현되지 않은 필드를 구현하기 위해 일회성으로 생성되는 클래스이다.<br>


- 다중 상속<br>
   - 여러 부모 클래스를 상속하는 것을 다중 상속이라고 한다.<br>
   JAVA는 모호성 때문에 다중 상속을 지원하지 않는다.<br>
   하지만 JDK8버전부터는 인터페이스에 default 메소드 선언을 허용하며,<br>
   여러 개를 지정할 수 있는 인터페이스 특성상 다중 상속을 지원하는 것이나 다름이 없다.<br>

- 모호성(ambiguity)
   - 하나의 자식이 여러 부모를 상속받을 때 부모 필드에 동일한 이름의 필드가 있다면,<br>
   어떤 부모의 필드인지 알 수가 없다. 이를 모호성이라고 부른다.<br>

- 모호성 해결 방법<br>
- 상황1 : 두 개의 인터페이스 내에 이름과 매개변수가 똑같은 메소드가 선언되어 있다.<br>
- 해결1 : 자식 클래스에서 재정의하여 사용한다.<br>

- 상황2 : 부모 클래스의 메소드와 인터페이스의 디폴트 메소드의 이름과 매개변수가 똑같이 선언되어 있다.<br>
- 해결2 : 부모 클래스의 메소드가 사용된다.<br>



- 함수형 인터페이스(Functional interface)<br>
   - 인터페이스 중 추상 메소드를 하나만 가지고 있는 인터페이스를 함수형 인터페이스라고 한다.<br>
   이 때 @FunctionalInterface를 인터페이스 위에 작성하여 단 하나의 추상 메소드만 선언할 수 있도록 제한해야 한다.<br>

- 람다식(Lambda Expression)<br>
   - 이름이 없는 메소드로서 변수처럼 사용이 가능하며, 매개변수로도 전달이 가능하다.<br>
   함수형 인터페이스는 추상 메소드가 한 개만 선언되기 때문에 메소드 이름이 필요 없다.<br>
   따라서 람다식을 익명 메소드(Anonymous Method)라고도 부른다.<br>

- 람다식 문법<br>
   1. (매개변수 형식 나열,...) -> 리턴값;<br>
   2. (매개변수 형식 나열,...) -> {2개 이상의 문장 작성; return 리턴값;}<br>


## 예외 처리<br>
   에러 : 심각한 오류<br>
   예외 : 덜 심각한 오류<br>


예외 처리 문법<br>
   try {<br>
      예외가 발생할 수 있는 문장<br>

   }catch(예외이름 객체명) {<br>
      예외 발생 시 실행할 문장<br>

      예외 발생 시 해당 예외 필드가 메모리에 할당된다.<br>
      할당된 주소를 선언한 객체로 받지 못한다면 프로그램이 강제 종료된다.<br>
      이를 막기 위해 동일한 예외 타입의 객체를 catch문 안에 선언하여 전달되는 주소를 잡아준다.<br>
      해당 예외 주소가 담긴 catch문의 문장이 실행된다.<br>

   }catch(예외이름 객체명) {<br>
      예외 발생 시 실행할 문장<br>
   }...<br>
   }finally {<br>
      예외 발생 여부에 상관없이 무조건 실행할 문장<br>
      ※ 외부 장치와 연결했을 경우 다시 닫을 때 주로 사용한다.<br>
   }<br>



## API(Application Programming Interface)
   개발에 필요한 라이브러리들의 집합.<br>
   선배 개발자들이 많어 놓은 소스코드.<br>

   - 내부 API<br>
      JDK 설치 시 제공해주는 기본 API<br>
      docs.oracle.com/javase<br>

   - 외부 API<br>
      선배 개발자들이 개발한 패키지 및 클래스들을 의미한다.<br>
      보통 JAR파일로 배포하며 자바 프로젝트의 buildPath에 추가하여 사용할 수 있다.<br>

JAR 파일로 배포하기<br>
   배포할 클래스 또는 패키지 우클릭<br>
   > Export > JAVA/JAR file 선택 > Next<br>
   > destination을 원하는 경로로 선택<br>
   > Export Java source files... 체크<br>
   > Finish<br>

JAR 파일을 프로젝트에 추가하기<br>
   배포된 JAR파일을 다운 받기<br>
   > 프로젝트 우클릭 > Build Path > Configure Build Path<br>
   > Libraries 탭 클릭 > ClassPath(안되면 ModulePath) 클릭 > Add External JARs<br>
   > 저장된 경로의 .jar파일을 더블 클릭으로 추가 > Apply 클릭<br>
   > Orders and Exports 탭 클릭<br>
   > Select All 클릭 > Apply and Close<br>


Object 클래스(최상위 부모 클래스, 모든 클래스는 자동으로 Object를 상속받는다)<br>
   1. toString()<br>
      항상 객체명을 출력할 때에는 toString()이 생략되어 있다.<br>
      toString()을 통해 출력되는 문자열이 마음에 들지 않는다면, 재정의하여 수정하도록 한다.<br>
      실무에서는 클래스 선언 시 각 필드의 초기화 여부를 확인하기 위해 toString을 재정의하여 사용한다.<br>

   2. equals()<br>
      주소값 비교(==).<br>
      String 클래스에서 equals를 값 비교로 재정의하여 사용하기 때문에<br>
      문자열 비교는 무조건 equasl()로 비교한다.<br>

   3. hashCode()<br>
  
  
 ## Set : 집합
 - 구현 클래스<br>
   HashSet<br>
      집합에서는 중복되는 원소를 포함할 수 없는 것 처럼 HashSet이라는 자료구조는 중복되는 값을 무시한다.<br>
      저장된 값들은 인덱스가 없기 때문에 순서가 없다.<br>
      값의 유무 검사에 특화되어 있는 자료구조이고<br>
      해시코드로 유무 검사가 진행되고 속도가 상대적으로 좋다.<br>

 - 순서 부여 : iterator()<br>
   순서가 없는 객체에 순서를 부여하거나, 순서가 있어도 iterator 방식의 순서로 변경하고자 할 때 사용한다.<br>
   hasNext()를 통해 다음 값이 있는 지 검사하고, next()를 사용하여 값을 가져온다.<br>

Set은 검사의 목적이 있기 때문에 순서 정보를 관리할 필요가 없어서 데이터 크기에 상관없이<br>
검색에 걸리는 시간이 매우 짧다.<br>
반면 ArrayList는 index를 관리해야하기 때문에 상대적으로 시간이 오래 걸린다.<br>
그러므로 기능적 차이가 없다면 Set을 사용한다.<br>



 ## Map
 - 구현 클래스<br>
   HashMap(서버 간 데이터 교환)<br>
      Key와 Value 한 쌍으로 저장되며, 검색의 목적을 가지고 있다.<br>
      Key는 중복된 값을 넣으면 Value가 최근 값으로 수정되고<br>
      중복되지 않은 값을 넣으면 새롭게 추가된다.<br>
      Value는 중복이 가능하다.<br>

## Thread
Thread 종료 방법<br>
   1. 필드에 boolean 타입의 변수를 선언하고 run()안에 있는 반복문에 해당 변수가 true일 경우 break 하도록 설계한다.<br>
   2. sleep() 또는 wait(), join() 등의 메소드를 통해 쓰레드 일시정지 상태일 경우<br>
       Thread객체.interrupt()를 사용하여 InterruptedException을 발생시킨다.<br>
       이 때 일시정지 시킨 메소드 부분의 catch를 통해 예외를 잡아주고 원하는 문장을 작성하면 된다.<br>
   3. 쓰레드를 일시정지하는 코드가 없을 경우 Thread.interrupted()의 상태를 확인한다.<br>
       Thread객체.interrupt() 사용 시 Thread.interrupted()의 상태는 true로 변경된다.<br>
   4. System.exit(0)를 사용하면 전체 쓰레드 종료(프로세스 종료)<br>

         
##    파일 입출력(Java Application 관점)<br>
   Stream이라는 연결통로를 통해 원본 데이터가 알맞는 인코딩 방식으로 전송된다.<br>
   byte단위로 입출력되기 때문에 개별처리이며, 상세 연산이 필요하지 않다면<br>
   Buffer를 사용한 입출력을 권장한다. Buffer를 사용하면 일괄처리가 가능해진다.<br>

   ※ 인코딩 방식<br>
      인코딩 방식은 완성형과 조합형이 있다.<br>
       - 완성형 : 각, 간, 갇, 갈, 감,..., 갛<br>
       - 조합형 : ㄱ + ㅏ + ㄱ<br>
      조합형이 효율적이며 byte단위로 데이터를 전송할 때 고정된 byte가 아니기 때문에 가변형 인코딩 방식을 선호한다.<br>
      조합형이면서 가변형인 인코딩 방식은 UTF-8이며, 전 세계에서 가장 많이 사용되는 방식이다.<br>

   Writer(출력)<br>
      BufferedWriter : 버퍼를 사용한 출력 클래스<br>
      FileWriter : 전달한 경로의 파일을 출력하기 위한 목적으로 열어준다.<br>
            전달한 경로에 파일이 없다면 새롭게 만든 후 열어준다.<br>

   Reader(입력)<br>
      BufferedReader : 버퍼를 사용한 입력 클래스<br>
      FileReader : 전달한 경로의 파일을 입력하기 위한 목적으로 열어준다.<br>
             전달한 경로에 파일이 없다면 오류가 발생한다(FileNotFoundException).<br>

   File(파일 정보)<br>
      전달한 경로에 있는 파일의 정보를 담는 타입.<br>
      디렉터리 생성, 해당 경로의 전체 파일 목록, 파일 삭제 등<br>



## 소프트 디자인 설계 패턴
 ▶ MVC <br>
 
   M(Model) : DB에서 조회된 결과 값을 담기 위한 변수들이 선언된 클래스<br>
         - 클래스명 뒤에 VO, DTO라는 문자열을 붙여준다.<br>
         - VO(Value Object) : 테이블을 보고 그대로 만든 객체<br>
         - DTO(Data Transfer Object) : 화면에 결과를 담아서 전달할 객체<br>

   V(View) : 사용자에게 보여질 화면을 구성하는 부분<br>
        - Controller에 선언된 CRUD 메소드를 사용하는 부분<br>

   C(Controller) : DB에 접근할 수 있는 메소드들이 선언된 클래스<br>
              - 접근 후 결과 값이 있을 경우 Model 객체에 담은 후 처리<br>
              - 클래스명 뒤에 DAO라는 문자열을 붙여준다.<br>
              - DAO(Data Access Object)<br>
