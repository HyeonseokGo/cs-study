# 프로그래밍 기초 지식 모음

## CS

### 프로세스와 스레드의 차이
프로세스 : 메모리에 올라와 실행되고 있는 프로그램의 인스턴스. 운영체제로부터 자원을 할당받는 작업의 단위. 다른 프로세스의 메모리에 직접 접근할 수 없음.

스레드 : 프로세스 내에서 실행되는 여러 흐름의 단위, 프로세스가 할당받은 자원을 이용함. Stack만 할당 받고 Code, Data, Heap 영역은 공유.

### 멀티 프로세싱 (운영체제)
여러개의 프로세서(대략적으로 CPU)가 서로 협력적으로 TASK를 처리하는 것. 즉, 여러개의 프로세서가 작업을 병렬적으로 처리하는 것. CPU가 추가되어 비용이 높아짐.

### 멀티 프로그래밍
특정 프로세스 처리 중, 낭비되는 시간에 다른 프로세스를 처리하는 것. 멀티 태스킹과 혼동 주의.

### 멀티 태스킹
프로세서가 다수의 TASK를 조금씩 번갈아가면서 수행하는 것. 사용자에게는 여러 TASK가 동시에 수행되는 것처럼 보임.

### 멀티 프로세스
하나의 프로그램을 여러개의 프로세스로 구성하여 각 프로세스가 하나의 작업을 수행하도록 하는 것.

장점 : 문제가 발생해도 다른 프로세스로 확산되지 않음. 

단점 : 프로세스간 통신이 복잡함. 높은 메모리 사용량 Context Swiching으로 인한 성능 저하.

### 멀티 스레드
하나의 프로세스에 여러개의 스레드를 구성. 각 스레드가 하나의 작업을 처리. 스레드간의 간단한 통신.

동기화 문제. 하나의 스레드에서 발생한 문제가 다른 스레드로 확산. 까다로운 디버깅.

### 멀티 스레드 동시성 제어 방법

### 교착 상태란
두 개 이상의 작업이 서로 상대방의 작업이 끝나기만을 기다리고 있기 때문에 결과적으로 아무 것도 완료되지 못하는 상태.

### 세마포어란

### Queue와 Stack
Queue : FIFO 방식으로 동작. 프로세스 처리, CPU 관리 등에 사용됨.

Stack : LIFO 방식으로 동작. 제거를 pop, 추가를 push라고 함.

### Heap이란
완전 이진 트리의 일종. 우선 순위 큐를 위해 만들어짐. 여러개의 값 중 최댓값이나 최솟값을 빠르게 찾아내도록 만들어짐.

반정렬 상태를 유지 (큰 값이 상위 레벨, 작은 값이 하위 레벨). 중복 허용.

최대힙 : 부모 노드의 키 값이 자식 노드의 키 값보다 크거나 같은 완전 이진 트리.

최소힙 : 부모 노드의 키 값이 자식 노드의 키 값보다 작거나 같은 완전 이진 트리.

### 이진트리란
트리의 요소 하나를 노드라고 함. 노드들끼리 부모 자식 관계를 형성. 최상단을 루트노트라고 함. 자식이 없는 노드를 단말노드라고 함. 트리 안에 존재하는 트리를 서브트리라고 함.

전위순회 : 루트 -> 왼쪽 서브트리 -> 오른쪽 서브트리

중위순회 : 왼쪽 서브트리 -> 루트 -> 오른쪽 서브트리

후위순회 : 왼쪽 서브트리 -> 오른쪽 서브트리 -> 루트

노드 i의 부모 : i/2

노드 i의 왼쪽 자식 : 2 * i

노드 i의 오른쪽 자식 : 2 * i + 1

### 이진탐색트리란

### 레드블랙 트리란

### 선택 정렬
첫번째 값을 두 번째 값부터 마지막까지 차례대로 비교하여 가장 작은 값을 찾아 첫번째에 놓고, 두번째와 이후 또한 이전과 같이 반복하여 정렬.

### 버블 정렬
서로 인접한 두 원소를 비교하여 정렬하는 알고리즘. 0 ~ n-1 까지 비교.

### 삽입 정렬
두번째 값부터 시작해 그 앞의 값과 비교하여 삽입할 위치를 찾아 삽입.

### 병합 정렬
배열을 크기가 1인 배열로 분할하고 합병하며 정렬을 진행.

### 힙 정렬
데이터를 힙 자로구조로 만들어 최댓값 또는 최솟값부터 하나씩 꺼내어 정렬. 전체 정렬이 아닌 가장 큰 값 몇개만 필요할 때 유용.

### 퀵 정렬
pivot을 설정하여 pivot보다 큰 값과 작은 값으로 분할하여 정렬.

### 빅오 표기법

### OOP란
컴퓨터 프로그램을 명령어의 목록으로 보는 시각에서 벗어나 여러개의 독립된 단위인 객체들의 모임으로 파악하는 것. 각각의 객체는 메세지를 주고받고, 데이터를 처리할 수 있음.

재사용과 확장에 용이. 캡슐화, 추상화, 다형성, 상속 등의 개념이 있음.

### 함수형 프로그래밍이란
자료 처리를 수학적 함수의 계산으로 취급. 상태와 가변 데이터 지양. 선언형 프로그래밍 패러다임을 따름.

데이터의 값을 변경하지 않으며, 객체의 필드를 설정하는 등의 작업을 하지 않는 순수 함수를 이용.

일급 객체, 고차 함수, 불변성, 순수 함수.

### 선언형 프로그래밍이란
명령형 프로그래밍이 어떻게 할 것인가에 초점을 두는데 반해, 무엇을 할 것인지에 초점을 두는 것.

선언형 프로그래밍을 위해 추상화가 필요.

### SOLID 원칙
단일 책임 원칙 : 한 클래스는 하나의 책임만 가져야함.

개방-폐쇄 원칙 : 소프트웨어의 구성 요소는 확장에는 열려 있으나, 변경에는 닫혀 있어야함.

리스코프 치환 원칙 : 서브 타입은 언제나 기반 타입과 호환될 수 있어야함.

인터페이스 분리 원칙 : 한 클래스는 자신이 사용하지 않는 인터페이스는 구현하지 말아야함.

의존성 역전의 원칙 : 고수준 모듈은 저수준 모듈의 구현에 의존해서는 안 된다. Ex) 자동차는 바퀴에 의존하면 안 됨.

### DI란
의존성 주입은 객체를 스스로 생성하는 것이 아닌, 외부에서 주입받는 것.

### OAuth란
다양한 플랫폼 환경에서 권한 부여를 위한 산업 표준 프로토콜.

### TCP, UDP 

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

### 공개 키 암호, 대칭 키 

### Clean Architecture란

## Kotlin

### Data Class
getter/setter가 없기 때문에 보일러 플레이트 코드가 줄어듬.

toString(), hashCode(), equals(), copy() 메소드가 기본적으로 구현되어 있음.

### Sealed Class
abstract 클래스로, 객체 생성 불가능. 생성자는 private. 하위 클래스와 동일한 파일에 정의되어야함.

when을 사용할 때, else 없이 사용할 수 있음.

Enum과의 차이점 : Enum은 Single Instance만 생성 가능.

### object란
kotlin 키워드 중 하나. java의 static을 대체. 싱글톤, 익명 클래스, companion object에 사용됨.

object 키워드로 싱글톤 클래스 선안. 상속 가능. 생성자 선언 불가능.

object 키워드로 익명 클래스 구현 가능. 싱글톤이 아님.

### Lambda와 고차 함수
고차 함수 : 함수를 인수로 받거나, 함수를 리턴하는 함수.

Lambda : 고차 함수에서 인수로 주어지는 식.

### inline class란

### crossline fun이란

### inline fun이란
Kotlin을 디컴파일 했을 때, 고차함수의 인스턴스를 생성하지 않고 코드를 함수 내부에서 바로 실행하도록 함.

인자로 전달받은 함수는 다른 함수로 전달 또는 참조가 불가능. noinline을 사용하여 해결 가능.

### noinline이란
inline으로 처리하고 싶지 않은 인자에 noinline 키워드를 붙여 제외할 수 있음.

### reified란

### by lazy, lateinit var 

by lazy : 호출 시점에 초기화. val만 사용 가능. immutable함. 기본 synchronized로 동작.

lateinit var : var만 사용 가능. mutable함. non-null. 초기화 전에 접근 시 Exception을 throw. setter/getter 정의 불가능. 원시 타입에서 사용 불가능.

## Java

### GC란?
유효하지 않은 메모리(참조되지 않는 객체)인 가비지 발생하는데, free()를 사용해 직접 메모리를 해제하는 C언어와 달리, 가비지 컬렉션이 알아서 메모리를 정리해줌.

Stop the world와 Mark and Sweep으로 진행되는데, JVM이 프로그램의 실행을 멈추고 메모리의 사용 여부를 식별한 후 해제하는 작업.

### 객체와 클래스의 차이
클래스 : 청사진. 

객체 : 클래스가 구현된 실체. 인스턴스라고도 불림.

### 기본형과 wrapper 클래스의 차이
wrapper 클래스 : 8개의 기본형을 객체 형식으로 다루기 위해 JDK에서 지원하는 8개의 클래스.

기본형 : 객체가 아님.

### call by value, call by reference 차이
call by value : 인자로 받은 값을 복사하여 처리.

call by reference : 인자로 받은 값의 주소를 참조하여 값을 직접 조작.

자바에서 기본 자료형은 call by value, 참조 자료형(Array, 클래스 인스턴스) 등은 call by reference.

### 직렬화란
메모리에 존재하는 정보를 쉽게 전달하기 위해 byte 형태로 변환하는 것.

### Stream
SE 8부터 추가된 개념. 데이터를 추상화. 데이터 소스를 변경하지 않음.

생성 -> 중개 연산 (변환) -> 최종 연산 (사용)으로 동작.

### equals()란
모든 자바 객체의 부모 객체인 Object 클래스에 정의되어 있음. Object에서 equals()는 각 객체가 참조하는 주소가 동일한지 검사하는 형태로 구현되어 있음. 객체의 비교에 사용할 때, 주소값이 아닌 객체의 값으로 비교하기 위해 재정의가 필요함. 재정의함으로써 Map의 Key와 Set의 원소로 사용 가능.

### equals()와 ==의 차이
equals()는 객체의 값 비교, == 은 주소 비교

kotlin에서는 == 이 내부적으로 equals() 호출. === 이 주소 비교.

### hashCode()란
일반적으로 각 객체의 주소값을 반환함. 재정의가 되지 않았을 때 HashMap의 Key로 사용된다면, hashCode() 값이 달라 Key로 검색하지 못함.

두 객체를 equals()로 판단하였을 때, 동일하다면 hashCode() 값도 동일해야한다. -> 재정의하여 사용.

equals()를 재정의하지 않고 hashCode()만 재정의한다면, 해시값으로 객체의 위치를 찾을 수 있지만 같은 객체인지 비교하지 못하기 때문에 null을 반환.

### String, StringBuffer, StringBuilder
String : 불변. 값이 수정될 때, 새로운 메모리 영역을 가리킴.

StringBuffer : 가변. thread-safe.

StringBuilder : 가변. 동기화 지원 X. 단일스레드에서 StringBuffer보다 좋은 성능.

### 정규 표현식이란

### 인터페이스
추상 클래스와 유사. 사용될 클래스가 어떤 메소드와 멤버를 가지는지에 대한 명세서. 클래스에서 구현.

### Array와 List의 차이

Array : 서로 연결된 데이터들이 순차적으로 저장. index와 값의 쌍으로 이루어져있음. 논리적 저장 순서와 물리적 저장 순서가 동일. index로 해당 원소 접근. 연속된 메모리 공간 사용. 정의와 동시에 크기가 정해지며 길이는 불변.

장점 : index를 통한 검색이 용이. 연속된 메모리를 사용하기에 관리가 편함.

단점 : 크기 고정 -> 삭제 시 빈 공간을 남겨두어야함. 정적이기 때문에 크기가 컴파일 전에 정해짐. 마찬가지로 크기는 불변.

List : 순서가 있는 요소의 모임. index를 버리는 대신 빈 공간을 허용하지 않음. index는 단순히 몇 번째 데이터인가를 나타냄. 불연속적으로 메모리 공간을 차지. 포인터를 통해 접근 가능.

장점 : 포인터가 다음 데이터를 가리키고 있기 때문에 삽입/삭제 편리. 동적임. 메모리 재사용 편리.

단점 : index를 통한 접근이 불가능하기 때문에 검색 성능 하락. 

### 컬렉션의 종류
Set : 중복 X, 순서 X

List : 중복 허용. 순서 유지. List는 인터페이스로 구현체로는 ArrayList, LinkedList, Hash가 있음.

    ArrayList : 내부적으로 Array 사용. 데이터 추가 시 해당 배열에 set. 연속된 메모리 공간 사용.

    LinkedList : Node와 Node를 연결하는 링크로 이루어짐. 데이터 추가/삭제 시 ArrayList보다 좋음. 하지만 검색 시 해당 노드까지 접근해야 하므로 성능 감소.

Map : Key와 Value로 이루어짐. 순서 X. Key 중복 X.

    HashMap : 중복된 Key 사용 시 기존 값 대체.

    HashTable : Key를 해시함수로 계산하여 그 값을 배열의 인덱스로 사용. Thread-safe. null x. Hash 값 충돌 시 LinkedList 형태로 변환.

### Hash Collision이란

### OKHttp3
Squar의 오픈 소스 라이브러리. HTTP 통신. HTTP Method를 쉽게 구현할 수 있음. 

### RxJava란
관측 가능한 스트림을 사용한 비동기 프로그래밍용 API.

Reactive programming 패러다임을 자바에서 구현한 라이브러리. 비동기 프로그래밍, 함수형 프로그래밍 기법 사용. 데이터를 생산하는 Observable와 소비하는 Subscriber.

### RxJava Single, Flowable, Maybe, Completable이란

## Android

### Dalvik란

### ART란

### intent란
컴포넌트 간 작업 수행을 위한 정보 전달에 사용됨.

명시적 : 클래스 객체나 컴포넌트 이름을 지정하여 호출될 대상을 지정하는 것.

암시적 : 다른 응용 프로그램의 컴포넌트를 호출할 때 사용됨. 호출할 대상의 속성을 지정.

### Pending Intent란
intent를 가지고 있는 객체. intent를 보류, 특정 시점에 작업 요청. Ex) Notification 클릭 시 intent 실행.

### 4대 컴포넌트
Activity : UI를 담당하는 컴포넌트.

Service : 백그라운드 작업을 실행하는 컴포넌트. Main Thread에서 실행됨.

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

### Doze 모드란
6.0(API 23)부터 추가된 기능. 기기를 오랫동안 사용하지 않는 경우 앱의 백그라운드 CPU 및 네트워크 활동을 지연, 배터리 소모를 줄여줌.

전원을 충전하고 있지 않고, 화면을 끈 상태로 기기를 일정 기간 정지 상태로 두면 시작됨.ㅇ

### gradle이란
유연성과 성능에 중점을 둔 오픈소스 빌드 자동화 도구.

### gradle implementation, api 차이
implementation : 의존 라이브러리 수정 시 본 모듈까지만 재빌드. A(impl) <- B <- C 의 상황에서 C는 A에 접근 X. A 수정 시 B까지 재빌드.

api : 의존 라이브러리 수정 시 본 모듈을 의존하는 모든 모듈 재빌드. A(api) <- B <- C의 경우 C에서 A 접근 가능. A 수정 시 B, C 모두 재빌드.

### minSdk, compileSdk, targetSdk

minSdk : 앱이 지원하는 가장 낮은 버전.

compileSdk : 컴파일 때 gradle이 사용할 안드로이드 sdk 버전. 해당 버전에 포함된 API 사용 가능.

targetSdk : minSdk 이상에서 지원하는 특정 기능을 사용하기 위함. 컴파일에 관여 X. 해당 버전까지 동작을 보장함.

### AndroidManifest란
어플리케이션에 관한 필수 정보를 안드로이드 플랫폼에게 알려줌.

### SharedPrefrences란

### SharedPrefrences commit과 apply 차이

### Context란
현재 실행 중인 어플리케이션 또는 Activity에 대한 정보 가진 객체.

### Intent
명시적 Intent : 클래스 객체나 컴포넌트 이름을 지정하여 호출할 대상을 지정. 어플리케이션 내부에 사용.

암시적 Intent : 호출할 대상이 달라질 수 있음. Ex) 메일, 인터넷 브라우저 선택 등.

### Content Provider와 Content Resolver의 차이
Content Provider : 어플리케이션의 데이터를 공유하기 위한 것.

Content Resolver : Content Provider에 접근할 때 사용하는 것.

### proguard란
코드 난독화 및 멀티덱스 방지 툴.

### consumerProguardFile

### 안드로이드 스튜디오의 Thread
Main Thread (UI) : 액티비티와 컴포넌트의 사용을 담당하고 연동하는 역할. 시스템 콜백, 이벤트 또는 Lifecycle과 관련있는 것은 Main Thread에서 처리해야함.
다른 작업에 의해 Main Thread가 지연된다면 ANR이 발생.

Worker Thread : 네트워크 또는 데이터베이스 쿼리와 같이 오래 걸리는 작업을 처리하는 Thread.

### Lopper
주시적으로 메시지 큐를 확인, 메세지나 Runnable이 존재한다면 Handler로 보내 처리 요청.

### Handler란
Thread의 메세지 큐에 메세지를 보내거나 수신된 메세지를 처리할 떄 사용됨. Runnable 객체를 전송할 수도 있음.

Handler 객체를 생성한 Thread와 해당 Thread의 메세지 큐에 바인딩됨.

### Runnable이란
Thread간 메세지를 정의하고 전달하고 수신 후 식별하는 번거로운 과정을 줄이기 위해, 실행 코드를 전송하기 위한 것. 실행 코드가 담긴 객체.

### Android Service와 Intent Service 차이
Android Service : Main Thread에서 동작. 오래 걸리는 작업을 실행하기 위해 별도의 Thread 생성이 필요.

IntentService : 별도의 Thread에서 동작. 오래 걸리지만 Main Thread와 관련 없는 작업.

### Service와 Thread의 차이점
Thread : Main Thread를 블락하지 않기 위한 작업 등으 처리. Foreground. 앱 프로세스가 종료되면 종료.

Service : Main Thread에서 실행됨. 사용자와 상호작용하지 않고 수행되는 Background 작업에 적합. 앱 프로세스가 종료되면 시스템이 자동으로 재시작.

### startService() bindService() 차이

startService() : Service 실행 후 직접적인 접근 X. 앱 종료 시에도 계속 실행.

bindService() : Service 안의 onBind 메서드와  Service 인스턴스를 통해 통신 및 접근 가능. 종료 시 자동으로 unbind 처리.

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

    권한 : 필요 없음, 다른 앱 저장소 접근 시 WRITE/READ_EXTERNAL_STORAGE
  
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
앱이 실행됨과 동시에 생성됨. Singleton. 각 컴포넌트에서 context를 이용한 접근이 가능.

### ViewModel을 사용하는 이유
UI에 보여지는 데이터를 수명주기에서 분리하여 저장하기 위해 만들어짐.

### Picasso vs Glide
Picasso : Glide에 비해 화질이 좋음. 많은 메모리 사용량. 캐시에서도 비슷.

Glide : 메모리 사용량이 적음.

### RecyclerView vs ListView

### ListAdapter란
DiffUtil을 간편하게 구현.

### Hilt란
Dagger를 기반의 DI 라이브러리. 컴파일 시점에 어노테이션을 읽고 class 파일을 생성해 의존성을 주입.

Dagger보다 러닝 커브가 낮음. 런타임 에러가 발생하는 Koin보다 안정성이 높음.

### Coroutine
동시성 프로그래밍을 지원하는 kotlin의 기능. 서로 협력하는 루틴. 네트워크 처리 같은 비동기 처리에 사용됨.

루틴 : 컴퓨터 프로그램에서 하나의 정리된 일. 보통 프로그램은 크고 작은 여러가지 루틴을 조합.

메인 루틴 : 프로그램 전체의 중요한 동작 절차를 표시.

서브 루틴 : 반복되는 특정 기능을 모아 별도로 묶어 이름을 붙인 것. 진입 지점과 탈출 지점이 명확. 함수와 비슷한 개념.

Coroutine : 메인-서브 개념이 없음. 루틴 진행 중 탈출, 다시 돌아와 나머지 루틴 수행 가능. 진입점과 탈출점이 여러개.

### CoroutineContext란
Coroutine을 어떻게 처리할 것인지에 대한 여러가지 정보를 포함하는 인터페이스.

### CoroutineScope란
Coroutine Block을 생성. 하나의 CoroutineContext를 멤버 변수로 갖는 인터페이스.

### lifecycleScope, viewModelScope, GlobalScope

### Job이란
launch() 함수에서 반환. Coroutine을 취소하거나 완료를 대기할 수 있음.

### launch란
새로운 Coroutine 생성. Job 리턴.

### async란
새로운 Coroutine 생성. Deferred를 리턴. 같은 scope에서 하나가 에러가 발생하면 나머지 자식에서 처리 실패.

Deferred는 await()를 사용해 사용해 원하는 시점에 결과를 return 받을 수 있음.

### suspend fun이란
Coroutine의 실행을 중지함. suspend 함수가 실행되는동안 Coroutine을 탈출, suspend 함수가 반환되면 다시 Coroutine을 재개한다.

### Flow란
단일 값만 반환하는 suspend fun과 달리 여러 값을 순차적으로 내보낼 수 있는 것. Rx와 비슷함.

생산자가 값을 생산, 소비자가 사용.

### Hot Flow, Cold Flow란.

### StateFlow, SharedFlow란

### Room이란
SQLite에 대한 추상화 레이어를 제공하여 원활한 데이터베이스 액세스를 지원하는 동시에 SQLite를 완벽히 활용.

### Jetpack이란

### AAC란

## Git

### git이란
