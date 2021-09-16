# 프로그래밍 기초 지식 모음

## CS

### 프로세스와 스레드의 차이
프로세스 : 메모리에 올라와 실행되고 있는 프로그램의 인스턴스. 운영체제로부터 자원을 할당받는 작업의 단위. 다른 프로세스의 메모리에 직접 접근할 수 없음.

스레드 : 프로세스 내에서 실행되는 여러 흐름의 단위, 프로세스가 할당받은 자원을 이용함. Stack만 할당 받고 Code, Data, Heap 영역은 공유.

### Queue와 Stack
Queue : FIFO 방식으로 동작. 프로세스 처리, CPU 관리 등에 사용됨.

Stack : LIFO 방식으로 동작. 제거를 pop, 추가를 push라고 함.

### Https란
패킷이 암호화 되어 있기 때문에 보안에 좋음.

### Http Request Code
1xx : 요청을 받았으며 작업을 계속함.

2xx : 성공.

3xx : 요청을 마무리하기 위해 추가 동작이 필요.

4xx : 클라이언트 요청 오류.

5xx : 서버 오류.

### Restful API란
REST의 속성을 가지는 API.

REST : Representational State Transfer의 약자. 웹 상의 자원들을 HTTP URI의 형태로 표현하고 URI 형식으로 HTTP Method(GET, POST, PUT, DELETE)를 통해 조작할 수 있는 아키텍처.

## Kotlin

### Data Class
getter/setter가 없기 때문에 보일러 플레이트 코드가 줄어듬.

toString(), hashCode(), equals(), copy() 메소드가 기본적으로 구현되어 있음.

### Sealed Class
abstract 클래스로, 객체 생성 불가능. 생성자는 private. 하위 클래스와 동일한 파일에 정의되어야함.

when을 사용할 때, else 없이 사용할 수 있음.

Enum과의 차이점 : Enum은 Single Instance만 생성 가능.

### Lambda와 고차 함수
고차 함수 : 함수를 인수로 받거나, 함수를 리턴하는 함수.

Lambda : 고차 함수에서 인수로 주어지는 식.


## Java

### GC란?
유효하지 않은 메모리(참조되지 않는 객체)인 가비지 발생하는데, free()를 사용해 직접 메모리를 해제하는 C언어와 달리, 가비지 컬렉션이 알아서 메모리를 정리해줌.

Stop the world와 Mark and Sweep으로 진행되는데, JVM이 프로그램의 실행을 멈추고 메모리의 사용 여부를 식별한 후 해제하는 작업이다.

### 객체와 클래스의 차이
클래스 : 청사진. 

객체 : 클래스가 구현된 실체. 인스턴스라고도 불림.

### 기본형과 wrapper 클래스의 차이
wrapper 클래스 : 8개의 기본형을 객체 형식으로 다루기 위해 JDK에서 지원하는 8개의 클래스.

기본형 : 객체가 아님.

### Stream


### equals()란
모든 자바 객체의 부모 객체인 Object 클래스에 정의되어 있음. Object에서 equals()는 각 객체가 참조하는 주소가 동일한지 검사하는 형태고 구현되어 있다. 객체의 비교에 사용할 때, 주소값이 아닌 객체의 값으로 비교하기 위해 재정의가 필요함. 재정의함으로써 Map의 Key와 Set의 원소로 사용 가능.

### hashCode()란
일반적으로 각 객체의 주소값을 반환함. 재정의가 되지 않았을 때 HashMap의 Key로 사용된다면, hashCode() 값이 달라 Key로 검색하지 못한다.

두 객체를 equals()로 판단하였을 때, 동일하다면 hashCode() 값도 동일해야한다. -> 재정의하여 사용.

equals()를 재정의하지 않고 hashCode()만 재정의한다면, 해시값으로 객체의 위치를 찾을 수 있지만 같은 객체인지 비교하지 못하기 때문에 null을 반환한다.

### String, StringBuffer, StringBuilder
String : 불변. 값이 수정될 때, 새로운 메모리 영역을 가리킴.

StringBuffer : 가변. thread-safe.

StringBuilder : 가변. 동기화 지원 X. 단일스레드에서 StringBuffer보다 좋은 성능.

### 인터페이스
추상 클래스와 유사. 사용될 클래스가 어떤 메소드와 멤버를 가지는지에 대한 명세서. 클래스에서 구현.

### 컬렉션의 종류
Set : 중복 X, 순서 X

List : 중복 허용. 순서 유지. List는 인터페이스로 구현체로는 ArrayList, LinkedList, Hash가 있음.

  ArrayList : 내부적으로 Array 사용. 데이터 추가 시 해당 배열에 set. 연속된 메모리 공간 사용.

  LinkedList : Node와 Node를 연결하는 링크로 이루어짐. 데이터 추가/삭제 시 ArrayList보다 좋음. 하지만 검색 시 해당 노드까지 접근해야 하므로 성능 감소.

Map : Key와 Value로 이루어짐. 순서 X. Key 중복 X.

### OKHttp3
Squar의 오픈 소스 라이브러리. HTTP 통신. HTTP Method를 쉽게 구현할 수 있음. 

## Android

### 4대 컴포넌트
Activity : UI를 담당하는 컴포넌트.

Service : 백그라운드 작업을 실행하는 컴포넌트.

Broatcast Receiver : 기기에서 발생하는 다양한 이벤트, 정보를 받는 컴포넌트.

Content Provicer : 다른 APP에서 앱 내부 데이터에 접근할 수 있도록 제공해주는 컴포넌트.

### Activity Lifecycle
onCreate : 첫 생성 때 호출. 뷰 생성. Activity의 이전 상태가 저장된 경우, 해당 객체가 번들로 제공됨.

onRestart : Activity가 중단되었다가 다시 시작되기 직전에 호출됨.

onStart : Activity가 사용자에게 표시되기 직전에 호출됨.

onResume : Activity가 시작되고 사용자와 상호작용하기 직전에 호출됨.

onPause() : 시스템이 다른 Activity를 시작하기 직전에 호출됨. 진행되고 있던 작업을 중단하는 데 사용됨.

onStop() : Activity가 더 이상 사용자에게 표시되지 않음. 아직 Activity 객체가 살아있음.

onDestroy() : Activity가 소멸되기 전에 호출됨.

### AndroidManifest란
어플리케이션에 관한 필수 정보를 안드로이드 플랫폼에게 알려줌.

### Context란
현재 실행 중인 어플리케이션 또는 Activity에 대한 포괄적인 정보를 지닌 객체.

### Content Provider와 Content Resolver의 차이
Content Provider : 어플리케이션의 데이터를 공유하기 위한 것.

Content Resolver : Content Provider에 접근할 때 사용하는 것.

### 안드로이드 스튜디오의 Thread
Main Thread (UI) : 액티비티와 컴포넌트의 사용을 담당하고 연동하는 역할. 시스템 콜백, 이벤트 또는 Lifecycle과 관련있는 것은 Main Thread에서 처리해야함.
다른 작업에 의해 Main Thread가 지연된다면 ANR이 발생.

Worker Thread : 네트워크 또는 데이터베이스 쿼리와 같이 오래 걸리는 작업을 처리하는 Thread.

### Handler란



### Android Service와 Intent Service 차이


### Service와 Thread의 차이점
Thread는 Main Thread를 블락하지 않기 위한 작업 등으 처리. Foreground.

Service는 Main Thread에서 실행됨. 사용자와 상호작용하지 않고 수행되는 Background 작업에 적합.

### LiveData란
Lifecycle에서 관찰 가능한 데이터 홀더 클래스. 

### DataBinding이란
프로그래매틱 방식이 아닌, 선언적 형식으로 레이아웃의 UI 구성요소를 앱의 데이터 소스와 결합할 수 있는 라이브러리.

### 저장소 (Q 이전)
내부 저장소 (개별 앱 공간) :
 
 권한 : 필요 없음
 
 접근 : getFilesDir(), getCacheDir()
 
 앱 삭제 시 제거 : O
 
외부 저장소 (개별 앱 공간) :

  권한 : 필요 없음
  
  접근 : getExternalFilesDir(), getExternalCacheDir()
  
  앱 삭제 시 제거 : O
 
외부 저장소 (공용 공간) :
  
  권한 : WRITE_EXTERNAL_STORAGE, READ_EXTERNAL_STORAGE
  
  접근 : getExternalStoragePublicDirectory()
  
  앱 삭제 시 : X
  
### 저장소 (Q 이후)
내부 저장소는 동일. 외부 저장소는 보안상의 이유로 다른 앱의 개별 공간에는 접근 X.
 
공용 미디어 저장소 :
  
  권한 : 다른 앱이 생성한 파일에 접근할 때 READ_STORAGE
  
  접근 : MediaStore
  
  앱 삭제 시 : X

### Application 클래스란


### ViewModel을 사용하는 이유
UI에 보여지는 데이터를 수명주기에서 분리하여 저장하기 위해 만들어짐.
