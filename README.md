# Cplusplus-Basic-Stiffening
* https://ansohxxn.github.io/cpp/chapter3-1/ --> C++연산자 총 정리

함수는 뒤에 () 즉, 괄호가 나와야함. 그렇지 않을 시 객체 

#include <iostream> 선언이유↓
iostream은 C++에 있는 입출력을 위한 헤더 파일이다. 이는 C++ 표준 라이브러리의 하나이다. Input/Output Stream에서 이름을 따왔다. 
C 프로그래밍 언어의 stdio.h와 같은 역할을 한다.

using namespace std; 선언이유↓
std는 클래스이다. using namespace std;를 선언해줘야 여러가지 함수를 올바르게 사용할 수 있는데, 
c와 달리 c++은 클래스로 이루어져 있어 그 중에 std라는 클래스를 사용하는 것을 명시하기 위해 설정해 주는 것이다.
using namespace std; 안 했을 시↓
 ex) std::cout << "Hello World" ; 와 같이 함수를 사용할 때 앞에 std::를 일일이 다 붙여줘야 함

int (정수)
 ex) int a = 1;
  해설 - a에 1이라는 정수 값이 들어감. 소수값은 사라짐.
double (실수)
 ex) double b = 1;
  해설 - b에 1이라는 실수 값이 들어감. 소수값도 나타냄.
max (x, y) --> x, y 둘 중에 최대값 --> 3개 이상의 값을 비교할 때는 #include <algorithm> 선언 후 max ({x, y, z})식으로 나타내야 함
min (x, y) --> x, y 둘 중에 최소값 --> "
※include <cmath>의 사용으로
pow (x, y) --> x의 y승 (power 거듭제곱)
sqrt (x) --> x의 제곱근
abs (x) --> x의 절댓값
round (x) --> x를 반올림한 값
ceil (x) --> x를 올림한 값
floor (x) --> x를 내림한 값

char (단일어) --> 연산자도 가능
 ex) char initial = 'A';
  해설 - initial에 A라는 단어가 들어감. 문자, 문자열은 나타나지 않음. 숫자를 넣을 수 있지만 숫자도 단일어 취급 됨.
string (문자열)
 ex) string name = "BRO";
  해설 - name에 BRO라는 단어가 들어감. 문자, 문자열은 나타냄. 숫자를 넣을 수 있지만 숫자도 문자열 취급 됨.
    +string함수로 변수를 선언한 다음 변수[배열] Or 변수.at(배열)식으로 사용 가능.
 ☞"변수.length()/clear()/append()" 등의 형태로 그 문자열의 길이나, 문자열에 들어간 데이터를 지우거나, 아니면 더 추가시키거
	할 수 있음
  .find('문자') --> 그 문자의 위치를 나타냄
  .erase(시작위치, 끝위치) --> 시작지점부터 끝지점까지의 문자를 삭제함
  .insert(위치, "문자") --> 지정한 위치 앞에 문자열을 삽입할 수 있음
  .at(위치) --> 지정한 위치의 문자를 나타냄

bool (참, 거짓)
 ex) bool switch = false;
  해설 - switch에 거짓을 부여
 ex) bool power = true;
  해설 - power에 참을 부여

const (고정, 정의)
 ex) const double PI = 3.14;
  해설 - PI에 3.14라는 실수 값을 고정시킴. 이 함수를 사용 후 뒤에 PI에 다른 값을 부여하면 오류가 발생.

namespace (이름 충돌 방지 해결)
 ex) namespace first { int x = 1; } --> cout << first::x ; (first에 부여한 x값 정수 1이 나타남.)
  해설 - 위의 식을 선언하고 난 후에 first::x를 선언 시 정수 1의 값을 나타냄.
    특징 - x라는 변수를 다양하게 활용할 수 있다. 위의 식을 선언 후 first::x를 선언하여 정수 1을 값을 나타내던, 
             namspace second { int x = 2;}를 선언하여 second::x를 선언하여 정수 2의 값을 나타낼 수도 있다.
※namespace에선 접두어를 사용해야 한다. (접두어란 first::x에서 first::이 부분)
 using을 사용하면 접두어를 사용하지 않아도 된다. 뜻 그대로 사용하겠다, 불러오겠다는 의미인 듯.
  ex) using namespace first; --> cout << x ; (first에 부여한 x값이 나타남.)
  ex) using namespace std; (std라는 클래스를 사용하는 것을 명시)

cout (output, 출력, 데이터를 콘솔 화면에 출력할 때 사용, 함수가 아님)
 << 연산 뒤에 피 연산자를 표현하면 알아서 출력
cin (input, 입력, 데이터를 사용자로 부터 받을 때 사용, 함수가 아님)  
 >> 연산 뒤에 피 연산자를 표현하면 받을 수 있음, enter를 누르기 전까지는 버퍼에 저장되어 있음.
endl (\n과 같은 개행문자)

getline (cin, 변수) (변수에 받는 값을 공백도 포함 시킴) <-- 전역함수 (cin.geline(변수,길이,끝)과 혼동x)
※문자열만 가능 (string 함수를 선언 했을 시에 가능)
  getline (cin , 변수)에서 cin 뒤에>>ws를 사용하면 getline을 사용하는 그 구문 보다 앞에 사용되는 구문과 구분하기에, 앞에 다른 구문이 있을 경우 사용 필수 

switch (변수) (하나의 변수에 여러개의 값에 일일히 부여를 해줘야 하는 경우 스위치 문 안에서 조건들을 부여하며 사용가능)
{
	case _ : (if와 같은 느낌 _에 들어가는 값이 변수와 일치할 경우  실행 --> break; 를 통해 case _에서 벗어날 수 있음)
          default : (else if와 비슷한 느낌, 위의  case를 통해 선언한 조건이 일치하지 않을 경우 실행)
}

3항 연산자 '?'
 식 ? 참일 때 : 거짓일 때 <-- 순으로 기재
   ex1) int x = 9;
     x%2 == 1 ? cout << "정답" : cout << "오답";
  ex2) int x = 9;
     x%2 ? cout << "정답" : cout << "오답"; --> 1일 때 참의 값, 0일 때 거짓의 값
  ex3) bool hungry = true ; //트루가 1의 값을 가지니까 "배고파"가 나옴.
     cout << hungry ? "배고파" : "배 안고파";    
  ex4) cout << (hungry ? "배고파" : "배 안고파"); <-- 이렇게도 사용가능.
  
  while문, do while문 (둘의 차이는 do while루프는 do이후의 먼저 일부 코드의 블록을 수행 후 아래의 while(조건);에서의 조건을 판단 후 참일 경우 다시 do 이후의 코드의 블록을 실행시킨다.)
  while (조건)
  {
  	//조건이 참일 때 실행될 코드
  }
  do
  {
  	//조건이 참일 때 실행될 코드
  } while(조건); <-- do while문은 세미콜론 필요

for문
for (변수,변수제한,변수증가량) 
{
	//변수에 지정된 값에서 변수에 제한된 값까지의 변수 증가량을 통해 얻어 낸 횟수(반복해야만 하는 상황에서 특정 횟수) 만큼 반복함.
}

break; <--반복문을 중지시킴, continue; <-- 특정한 그 부분을 건너뛰고 반복문을 계속 진행시킴

모든 클래스는 타입으로 올 수 있다.
class 식별자(이름을 짓는 것) - 캡슐화
{
  //	접근저장자(접근제한자) : "public :" = 다 접근 가능, "private :" = 클래스 내부에서만 서로 접근 가능(외부는 차단),
	"protected :" = 클래스 내부에서만 서로 접근 가능, 클래스 밖에서는 오직 내 자손들만 접근 가능.
	접근지정자 생략시 자동으로 "private :" 지정. 
	
  // 총 네가지가 있음. 
	-멤버변수 : 클래스 안에서 선언된 변수(지역변수랑 다름)
	-생성자 : 클래스 명(식별자)이랑 똑같음, 리턴 타입이 없다, void를 적지 않는다, 주역할은 멤버변수 초기화, 클래스가 메모리에 자리 잡으면 그 때부터 객체라고 부른다, 객체가 메모리에 자리잡는 순간에 어떤 액션을 하고 싶으면 생성자 안에 코딩한다. 하지만 이 외에도 어떠한 일도 다 가능.
	-소멸자 : 객체가 메모리에 자리잡을 때 생성자가 수행된다면, 반대로 메모리에서 나갈 때 소멸자가 수행된다. 특징 : 생성자 앞	에 물결무늬
	-멤버함수(메소드 : 자바) : 교재에 따라서 생성자, 소멸자도 멤버함수에 포함시키기도 함. 
	  우리는 생성자 소멸자를 제외한 것을 멤버함수라고 함.
	 리턴할 거 없으면 리턴타입은 void라고 정확히 명시해야 함 
	
	소멸자는 오버로딩이 없음
	
	생성자와 소멸자 생략시 컴파일러가 알아서 생성자{}이런 식으로 생성함 소멸자도 동일.
	
	클래스는 소문자로 언급 -->Class Retage{} (x) class Retage{} (o)
	
	
} ; //클래스는 중괄호 닫고 세미콜론

-클래스 밖에서 (ex) main함수 안에서) 객체변수 선언하면  그 변수의 메모리에 자리 잡으면서 자동으로 생성자가 호출됨.
 따라서 만약 생성자의 접근지정자가 "public :"이 아니라면 변수가 생성 불가 할 수도 있다.
 객체변수가 선언되면 그 다음에 그 안에 있는 멤버변수, 멤버함수에 접근할 때는 "객체변수명.멤버변수(혹은 멤버함수)" 이렇게 사용.
 생성자와 소멸자는 객체변수명.생성자 이런 식으로x 메모리에 자리잡을 때 및 메모리에서 나갈 때 자동으로 호출.
-함수 안에서는 위부터 차례대로 번역하므로 코딩 순서가 중요. 하지만 클래스 내부에서는 코딩 순서가 상관x
 but 대부분 클래스 내부에서 순서를 맞추긴 함.

-딱히 다른 언급이 없이 cout을 선언 했을 시 정수부 소수부 상관없이 숫자 6개가 나옴.

-c언어(확장자가 .c인 경우) 에서는 struct안에 변수만. 
  c++(확장자가 .cpp인 경우) 에서는 struct랑 calss 같음(하지만 struct에서 접근지정자를 생략시 기본으로 "public :")

/ 메인함수 안에서 선언된 변수는 지역변수(객체변수). 이들은 스택, 즉 메모리에 차곡 차곡 코딩 순서대로 값이 저장됨. --> 변수가 생성된 중괄호가 사라질 때 소멸됨. 값을 넣는 것을 push, 나오는 것을 pop.

헤더파일에서 소스를 만들고 메인파일에서 그 헤더파일을 불러올 때 중복된 내용을 삭재하는 법
#ifndef 대문자이름
#define 대문자이름
~     // 소스 작성
#endif

스택은 늦게 생성된 것이 먼저 소멸됨.
	/* 주석 
		*/

	
