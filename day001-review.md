\#\# 180302\_day002



 ctrl + shift + F : 코드 자동 정렬

 코드에 에러가 있으면 정렬 못함



빨간 에러 -&gt; IDE에서 제공하는 디버거

\(에러라고만 하지 말고 디버거라고 할 수 있어야겠다 ㅎㅎ\)



!\[enter image description here\]\(https://lh3.googleusercontent.com/KTNmCZ02BwT2DgIChbvn561PeeOlKY9e8CBj7CVCoOiInGcjKIyXbLH953CQAgpsEIeBMupM0Ek\)



자바에서 주석 3가지

1. \`/\*내용\*/\` : 문단 주석

	- 이 주석은 /\*만 작성하면 이 이후 내용 다 주석처리 됨. 그리고 뒤에 내용 쓰는거 까먹어서 에러 발생 요인이 됨. 고로 // 쓰는 것을 추천

2. \`/\*\*내용 내용 내용\*/\` : 문서 주석

	- 전체적인 프로그램 개요 등, 문서화 시킬 때 사용 \(사용하는 상황이 좀 다름\)

3. \`//내용\` : 문장주석



 주석 범위 지정

 Ctrl + Shift + C 누르면 주석 설정 / 해제 가능

 -&gt; Ctrl + / 말고도 되네



!\[enter image description here\]\(https://lh3.googleusercontent.com/DY\_fis01WJy3pCr\_brxrHCtgy8hMG6vm5AOWtM9VLPJXLH\_HO\_kTeGddMiDgNCdhh\_erZvpnRAY\)



근데 범위 설정하여 주석 처리하고, 자동 정렬하고, 다시 주석해제하면 저기 위에처럼 줄이 잘 안 맞아.. 아 이러면 한번 더 자동정렬하면 되긴 하겠구나. 

만약 이런게 싫으면 커스텀을 해야 하는데 커스텀은 어떻게 할 수 있지? atom의 beautifulfy는 어떻게 만든거지

또 주석 처리 되어있는 곳에 또 주석 처리하게 되면 위에 ////처럼 중복으로 주석 처리 됨. 주석 해제하면 한번에 ////다 없어지는건 아니고 //만 없어지게 됨



----

속도의 문제가 아니라 정확성의 문제 때문에 자동 완성을 쓰는거구나

Ctrl + Space 자동 완성



변수 - 프로그램이 사용하는 데이터를 일시적으로 저장할 목적으로 사용하는 메모리 공간

직접적인 데이터를 뜻하는게 아니다

변수는 타입과 이름을 가지고 있음

-&gt; 나는 변수에 어느정도로 설명할 수 있을까, 생각해보니 설명할 수 있는 말이 없음을 깨닫고 강의를 열심히 듣기로 한다. 모르는게 속속 나온다.



타입 - 이 변수 공간에 뭐가 들어올 수 있는지 정해주는 것

따듯한용 컵, 이라고 하나의 타입을 고정시켜준다. 

보드마카 펜 파란색 펜 - 빨간색 잉크 넣으면? 불량이다. 

-&gt; 오 이렇게 비유를 하니 재밌다. 또 '하나의 타입을 고정시켜준다'라는 개념. 기억해야 할 부분인 듯



변수 : 타입 + 변수명

정수 : int 변수명; //바구니, 컵의 이름을 x라고 하겠다!

이게 선언이다. 메모리 공간에다가 여기는 x꺼야, 라고 선언함. 메모리의 할당을 받는 행위를 변수의 선언이라고 한다. 

-&gt; 오오. 선언의 의미 중요하지. 왜 선언이 필요하냐 - 메모리의 할당을 받는 행위!



변수가 뭐냐?

데이터를 넣기 위해 메모리에 공간 확보하기 위해, 데이터를 집어넣기 위한 공간이 변수다. 

\(변할 수 있는 수.. 는 이제 초등학생 ver임\)



수학에서는 x = 100; x와 100은 같다라는 이미지만 프로그래밍에서는 다르다. 

=\(대입연산자\)은 100\(값\)을 x\(변수\)에 담아라-라는 수식이다. 

같다는 의미는 ==로 표현한다. 

-&gt; 맞아맞아. 이거 헷갈리면 프로그램 버그 원인이 될 수 있지. 특히 if문에서 if x=10 으로 실수 많이했었지. 



int x; 를 함으로 일어나는 일

메모리에 int 정수가 들어올 수 있는 x라는 이름의 공간을 메모리에 할당해줘, 라고 운영체제에 말 하는 것. 그럼 운영체제가 보고 오케이. 메모리에 x라는 공간을 만든다. 



x = 100;

변수의 초기화 - 변수에 값을 넣는다.



절차지향

컴파일러가 위에부터 아래로 절차적으로 실행하게 되어있다.

그렇기 때문에 x 변수 공간을 메모리에 만들고, 그 다음 y 변수 공간 만들고, sum 변수 공간 만들고, 이제서야 x 변수 공간에 100이라는 값을 집어 넣는다. 



\`\`\`java

int x;

int y;

int sum;



x = 100;

y = 200;

\`\`\`



-&gt; 이 코드에서 메모리에 일어나는 변화! 굿굿 바닥부터 하는 설명 굿굿



위에 이어서 

\`\`\`java

sum = x + y; 

\`\`\`



책 24쪽 컴퓨터 구조

 

 변수는 프로그램이 실행되면서 영향을 받아 값이 바뀔 수 있는거고, 상수는 프로그램 실행되는동안 값이 바뀌지 않음

 -&gt; 변수쓸지 상수쓸지 정할 때 이 말을 참고해야지



스택 - 변수들은 다 스택에 들어가게 되어 있음



100이라는 숫자를 그냥 만드는게 아님

상수 영역에 100이라는 숫자를 만들어야 함

그 다음 그 100이라는 숫자를 x에 집어 넣게 되는 것임

그 다음 200을 또 만들어서 y값에 집어 넣고

CPU가 x랑 y를 가져와서 더한다!

-&gt; 아하 CPU가 이럴 때 또 나오는구나



컴퓨터 구조

CPU\(중앙처리장치\) -&gt; 연산장치

메모리\(주기억장치\)  -&gt; 저장장치

HDD\(하드디스크, 보조기억장치\) -&gt; 저장장치



메모리는 잠깐동안 가지고 있을 수 있는 공간

하드디스크에 있는 값을 CPU에 보내 연산하려고 하는데 하드 속도 너무 느려서 CPU 연산 속도 따라잡지 못함. 그래서 그 속도 단차 따라잡기 위해 메모리 생김. \(메모리도 CPU보다는 느림\) 



- 프로그램이 설치가 되어 있다?

	- 보조기억장치에 저장 되어있다 라는 소리.

- 프로그램이 실행중이다?

	- 주기억장치에서 필요한 데이터가 로드되어 있는 것을 말함.

- 프로그램이 동작중이다?

	- CPU에서 뭔가를 연산중이다!



-&gt; 오오오오 기초지식, 이 차이 재밌다.



\`\`\`java

sum = x + y;

\`\`\` 

jvm 이 OS에 명령을 보내는데 cpu에 x랑 y 좀 더해줘

cpu가 x야!!! 부르면 메모리에서 쨘 하고 오고 \(아 부르는거 너무 귀여움 ㅋㅋㅋㅋ\)

y야!!! 하고 부르면 메모리에서 쨘 하고 오고

이 결과값 300은 상수를 거치지 않고 스택으로 바로 저장된다!

따라서 상수값에 300 저장되지 않는다!



변수 이름은 프로그램 단 한 놈만 있어야 한다. \(unique 해야 한다\)



코드 짧게 쭐이라 쭐이라 너무 연연하지 말라. 

정답만 무슨 짓을 해서든 만들면 된다. \(우선은\)

짧은게 무조건 답은 아니다. 



----



자바에서 .은 그 꾸러미 안에 있는 내용 쓰겠다는 말 

jre 꾸러미에서 System 이라는 놈 꺼내서 out 이라는 놈을 꺼내서 그 out 안에 println이라는 기능을 꺼내서 사용을 하겠다, 라는 의미

-&gt; . 접근 연산자라고 불렀었나? 



system이라는 얘기는 pc OS에서 모든 기능을 제공하는 애, 이 시스템의 표준, 가장 기초, 입력과 출력을 받을 수 있는 것, 운영체제 기능 빌려서 쓰는 것. 표준 입력과 출력에 대해서. 



키보드! 입력을 하는걸 표준 입력이라고 함 \(마우스는 ㄴㄴ임\)

출력은 모니터! 



ln = line next 약자



Scanner는 입력 데이터\(키보드 입력\) 편리하게 가공해주는 도우미 꾸러미

System.in 요기로 들어온 데이터\(값\)을 가공해줌



!\[20180302115422.png\]\(https://photos-5.dropbox.com/t/2/AADEbBgrjHacSrHfBet29H55pDfb\_sf7-FYUw67ajMNbHQ/12/875438832/png/32x32/1/\_/1/2/20180302115422.png/EKDQ87gJGIIHIAcoBw/H2gMmwP7hGvyUrJF3odS2LK0jcxwGPXLbUW9KWwSmlw?preserve\_transparency=1&size=800x600&size\_mode=3\)



System. 꾸러미는 필수적인 기능의 꾸러미. 그냥 언제든지 쓰고 싶을 때 쓸 수 있음.



Scanner 꾸러미는 외부에 있어서 import라는 놈을 선언해서 사용할 수 있음



!\[enter image description here\]\(https://lh3.googleusercontent.com/Av2\_3Jgq50EGsKAm9vApC3RXwQnOhv-DJ1eKbOP842DCIDGqSEZC8Ehs8hzge11gPsxwwIQQ1x8\)



// 외부 기능 꾸러미를 우리 프로그램에서 사용할 수 있도록 가지고 옴.

// 이놈은 java에서 제공함. 어떻게 알아? java 라는 꾸러미에서 util 꾸러미에 Scanner가 있습니다, 명시해주는 것.

// rt = runtime 





!\[20180302120606.png\]\(https://photos-2.dropbox.com/t/2/AABytHWrD4PtdrnUf0k7Fgyr6IemvGMeLxORgAL\_g3thbA/12/875438832/png/32x32/1/\_/1/2/20180302120606.png/EKDQ87gJGKgHIAcoBw/cnBz620WEkQrH7HF-e587xYg3qKUy4Wq1V8GJ-n8TVg?preserve\_transparency=1&size=800x600&size\_mode=3\)



input!!!!하고 변수명 부르면 scanner가 뛰어 나옴 ㅋㅋㅋ

Scanner는 타입, input은 이름



Scanner input; 선언 완료

; 세미콜론 - 반드시 문장 끝에는 찍어줘야 함





인터페이스가 뭐냐

-&gt; 아 왜 대답 짜치게 했냐 흑흑



안쓰는데 왜 만들까? 변수들

만들긴 만드는데 왜? 쓰지도 않는데

위에서 절차적으로 내려오니까 아래에서 쓰는지 안 쓰는지 모르니까 만든다.

마지막까지 절차지향적으로 내려오니까. 위에서는 아래에서 이게 쓸건지 안 쓸건지 어떻게 알아? 모르지.



!\[20180302122049.png\]\(https://photos-3.dropbox.com/t/2/AADCFysYvWypnTZ6vk82Z4ShVvjXJ83ff-m9VIVryUgU7A/12/875438832/png/32x32/1/\_/1/2/20180302122049.png/EKDQ87gJGOYHIAcoBw/mksUOugSekrIAtCskCFng6E4sFPxoP\_jUdOJ946zw2U?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[enter image description here\]\(https://lh3.googleusercontent.com/3CaBTVcjgGHqgZN9gYTP8ZdI\_wOm1qbnkcJNsT8otsbHSotiEtQrScynaQT-9YY-GRvBAxkFjmo\)



input. 하면 스캐너에서 쓸 수 있는 기능 쭈루룩 나온다. 여기 설명 꼭 보아라





----



!\[20180302124056.png\]\(https://photos-6.dropbox.com/t/2/AACsN7EnK6urBpsMpB217wE9SqWFuhKrowtsHb\_fAFIUOQ/12/875438832/png/32x32/1/\_/1/2/20180302124056.png/EKDQ87gJGPoHIAcoBw/T61nVOdGofUo80hE9lEI7csDIHjHLrMkJX2Tl4GV9eU?preserve\_transparency=1&size=800x600&size\_mode=3\)







!\[20180302124802.png\]\(https://photos-3.dropbox.com/t/2/AAAlAwHmpqNDsC0qvOLh644-AlBH8h29o1ktBXUYWt9M8Q/12/875438832/png/32x32/1/\_/1/2/20180302124802.png/EKDQ87gJGJEIIAcoBw/OQPfAiQZmJqLUDtFK84euqh1SLIRprNCUq7nBNNHVOs?preserve\_transparency=1&size=800x600&size\_mode=3\)



-&gt; 이 구조 꼭 이해하고 있어야 한다. 그래야 프로그래밍 할 수 있다!

콘솔에 20 입력하면 얘는 상수 거칠 필요 없이 바로 메모리 x로 들어갈 수 있음





문자랑 숫자를 같이 더하면 숫자가 문자가 되어서 더해짐. \(문자가 더 큰 범위이기 때문에\)

!\[20180302131010.png\]\(https://photos-6.dropbox.com/t/2/AAD5LUwFvQANjdvCeBHOn6cb\_aQUq6lMZnZVArPBPz73pQ/12/875438832/png/32x32/1/\_/1/2/20180302131010.png/EKDQ87gJGNQIIAcoBw/hjChTKbpWwwpJkfrnXNiDws8GFhXAV\_71FehyV0215c?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[20180302131442.png\]\(https://photos-5.dropbox.com/t/2/AAA8tF0lriIn4I\_agXhXAyQbqZg4buU7vqEhFlIDGuRoJw/12/875438832/png/32x32/1/\_/1/2/20180302131442.png/EKDQ87gJGPMIIAcoBw/HGNyInYfcg8ogVdvi6L8IONyZhHN2LKlAvQu0hVKGAM?preserve\_transparency=1&size=800x600&size\_mode=3\)



여기까지 코드~

\`\`\`java

import java.util.Scanner; 

// 외부 기능 꾸러미를 우리 프로그램에서 사용할 수 있도록 가지고 옴.

// 이놈은 java에서 제공함. 어떻게 알아? java 라는 꾸러미에서 util 꾸러미에 Scanner가 있습니다, 명시해주는 것.

// rt = runtime 



public class add2 {



	public static void main\(String\[\] args\) {

		

		//스캐너 들어올 공간만 있다. 스캐너 집어 넣어야 한다. 대입 연산자 이용하면 된다.

		Scanner input = new Scanner\(System.in\); //새로운 스캐너 쨘! 만들어 input 메모리 공간에 집어 넣기

		//System.in 표준입력 - 키보드 입력만 받을 수 있는 스캐너를 만들어서 input이라는 메모리 공간에 저장한다.

		

		int x; //첫번째 숫자 저장할 변수공간.

		int y; //두번째 숫자 저장할 변수공간.

		int sum; // 두 숫자 더한거 저장할 공간 필요

		

		System.out.print\("첫 번째 숫자 입력: "\);

		x = input.nextInt\(\);

		System.out.print\("\n"\);

		

		System.out.print\("두 번째 숫자 입력 : "\);

		y = input.nextInt\(\);

		System.out.print\("\n"\);

		

		sum = x + y;

		

//		System.out.println\(x\);

//		System.out.println\(y\);

		System.out.println\("x = " + x + ", " + "y = " + y\);

		System.out.println\(x + " + " + y + " = " + sum\);

		

		System.out.println\("안녕하" + 3\);

		

		//서식화된 출력 사용하기

		System.out.printf\("결과 : %d \n", sum\); //서식 문자열 쓰려면 반드시 printf 사용해야함. print, println 사용 못함

		//서식 문자열 그리고 콤마 이후에 인자값 중 첫번째를 십진수로 표현

		

		System.out.printf\("%d + %d = %d", x, y, sum\);

		

		

	}



}



\`\`\`

----

문제를 보면 키보드부터 두드리려고 하지 말고, 문제 해결에 무엇이 필요한지부터 '생각' 할 것, 미리 설계



오류의 종류

- 컴파일 오류

컴파일 하자마자 발견되는거, 이게 발견되는 이유는 디버거 

컴파일 전에 확인\(문법 맞지 않으면 컴파일 되기도 전에 퉤에엣-\)

	- semantic error : 문자에서 숫자 뺄 때 \(의미적으로 말이 안 됨\)

	- syntax error : 문법 잘못되었음 \(구분 말이 안 됨\)



runtime exception 네모 구멍에 세모 블록 넣는거랑 비슷한 상황

ex. int만 넣을 수 있는 숫자 입력에 문자 입력



- 컴파일 에러 : 컴파일을 실패한거 \(예를 들면 뭄법 오류\)

- 런타임에러 : 실행 중에 프로그램이 뻗어버림 \(정수 입력 해야하는데 문자열 넣는다거나...\)

- 논리 에러 : 컴파일, 런타임 에러도 없이 잘 돌아가는데 프로그램 결과값이 우리가 원하는게 아님...제일 나쁜놈....찾기 어렵다



컴파일에러 : 자동완성, 오타방지

런타임에러 : 충분히 테스트를 거치면 방지, 발견하여 막아낼 수 있음

로지컬에러 : 연습 ;; 하하하 ;;; 





데이터 타입은 기초형과 참조형으로 나뉨



!\[20180302151800.png\]\(https://photos-3.dropbox.com/t/2/AACaaUUGl\_-aAcJhPvUn-KAKh0LY4nWN\_5LBfuLHvYYqnw/12/875438832/png/32x32/1/\_/1/2/20180302151800.png/EKDQ87gJGNAJIAcoBw/GsYAduSqrUiiy4RR-gcjAUxzc8G7sazhyMJ8OyahOzU?preserve\_transparency=1&size=800x600&size\_mode=3\)



문자형 char에는 한 글자만 들어갈 수 있음 \(단어, 문장 ㄴㄴ\)



변수는 선언과 동시에 초기화 가능



!\[enter image description here\]\(https://lh3.googleusercontent.com/vPhDH0LXoDzbELPDfg1xrYCaIlGJpULcc6OY-roFxdZRo5LLIr4W\_UOAbZBWn9Gh1wa7-XvIwqg\)

""는 String에 문자 넣을 때 사용함. 즉 컴파일러가 "" String으로 인식하니까 char에서 에러가 나는 것. 

''로 사용하면 에러 안 남

-&gt; java는 ""랑 ''랑 구분 하는구나 . 앞은 문자열 뒤는 문자

\`\`\`java



public class type {

	public static void main\(String\[\] args\){

		

		char c = 'a'; //"a"는 문자열로 인식되므로 char보다 커서 에러 발생. 구분할 것

		

		System.out.println\("c"\);

		

		double a = 5;

		System.out.println\(a\);		



		//숫자로 시작하는 변수는 만들 수 없음

		//int 1c; 에러 발생

		

	}

}



\`\`\`

변수 이름은 식별자

\(identifier\)의 일종



- \[ \] 유니코드 뭔지 왜 만들었는지 확인~

http://studyforus.tistory.com/167

http://jinuine.blogspot.kr/2013/09/ms949.html

-&gt; 인코딩이 뭐지? 디코딩은?



이런이런 변수는 이런이름으로 할거야

설계하는 분이 보통 이런 변수들도 정리해서 주면 개발자가 바로 개발해서 사용할 수 있음

-&gt; 오오 디자인 리소스 이름 정하는게 이래서 또 중요하구나



변수명 관례

클래스명은 첫글자 대문자로 한다. \(고로 class만들 때 test로 하지 말고 Test로 만드는 습관 들이자\)

변수명, 메소드명은 소문자로 시작해서 이후 단어는 첫글자 대문자

red\_apple 조합문자처럼 변수 쓸 수도 있고.. 

상수는 모든 철자를 대문자로 씀



1바이트 = 8비트

1MB = 1024KB = 8,388,608비트



\*\`c에서는 0이나 1 논리값으로 쓰는데 자바는 아님!!! true or false\*



연산자 operator

값을 구하는 하나의 수식어.

 피연산자 operand

 그 연산에 당할 놈

!\[20180302155944.png\]\(https://photos-2.dropbox.com/t/2/AADmVLBVBuVz82rCMb9CgRAgNwB-klMI9LXF8x\_3ec2MhQ/12/875438832/png/32x32/1/\_/1/2/20180302155944.png/EKDQ87gJGL8KIAcoBw/6pBrSrCAw1YS\_cGs9TFzyqNVk233KuXmTAI5FifWK9I?preserve\_transparency=1&size=800x600&size\_mode=3\)



연산자 우선순위

!\[enter image description here\]\(https://lh3.googleusercontent.com/lgzWExCb3jzhVJ73K\_7bJvozaEewEBxEFfmAzB-GRLel84R6F3RSEFu1eWuSUH\_jQfVq\_jODVe4\)



!\[enter image description here\]\(https://lh3.googleusercontent.com/RZybxXSPrMcxC0YLC7P2ZlOx9Lyhz4wKJDWHwL\_2efXse1LkkQLhg1GFDoStuByGacGSWJ5OrWM\)

-&gt; 아 이래서 for\(int i; i &lt; 10; i++\) 이런 식으로 쓰는거구나



!\[enter image description here\]\(https://lh3.googleusercontent.com/o79w3bVGBKaYtG39urvHhzZyzXr-am2TsPu4EkFSY0SViIWB-hMUXWtWfd6sjypzJTrXKWMbAzg\)



그래서 이름이 단항 연산자구나 

두줄쓸거 한 번에 쓸 수 있다구 ㅋㅋ int nextX = ++x; 의미는 x = x+1; int nextX = x;



\`\`\`java

public class type {

	public static void main\(String\[\] args\){

		

		

		int x = 5;

		System.out.println\(x++\); //5출력하고 x값은 6

		x++; //x6에서 쓰고 1 올라가니까 7

		System.out.println\(x\); //x 7출력

		--x; //7에서 1 감소시키니까 6

		System.out.println\(x--\); //6출력하고 현재 x값 5

		System.out.println\(x\); //x값 5

				

	}

}

\`\`\`

-&gt; 틀렸어 젠장 ㅋㅋㅋ 다시 볼 것. 메모리 그려가면서



!\[20180302163911.png\]\(https://photos-1.dropbox.com/t/2/AACCUM2XCz2hHUrmZ9MfaQkn13OX3CAeqE\_deqSk1guF5w/12/875438832/png/32x32/1/\_/1/2/20180302163911.png/EKDQ87gJGI0LIAcoBw/wGlLeEeReieMcxdxIXg-V-AQmkliLFwx6Cme6HKRk6k?preserve\_transparency=1&size=800x600&size\_mode=3\)





!\[enter image description here\]\(https://lh3.googleusercontent.com/OsAwCan2669OIIPr1ZeJMAaLsWJBl03IlY1XYSzNO9B6\_mwWcIMFfEeOu4zlh8VxAvLbjUwVe4Q\)





!\[20180302164207.png\]\(https://photos-3.dropbox.com/t/2/AAAfu1oHc-AYHKdrjz3OoRy9rrc1cTLMwxoeg\_SbWGBzmw/12/875438832/png/32x32/1/\_/1/2/20180302164207.png/EKDQ87gJGJULIAcoBw/oosAUdscPC4zmLNl1aLvFhN7vv5KyT3ncYOIcU1EsRM?preserve\_transparency=1&size=800x600&size\_mode=3\)

굉장히 중요 ~

관계연산의 결과물은 항상 boolean값으로 나옴





condition 조건/상태 



삼항 연산자

\`condition? exp1 : exp2 //condition 참이면 exp1 실행, 거짓이면 exp2 실행\`

\`max\_value = \(x &gt; y\) x : y; //최대값 계산\` 

max는 x가 됨























 





















 

 























 

