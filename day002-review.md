\#\# 180304\_day002-review



- 콘솔에서 입출력 받을 수 있다. 

	\`\`\`java

	import java.util.\(기억 안남\)

	public InputEx {

		public static void main\(String\[\] args\){

			Scanner import = new Scanner\(System.in\);

			System.out.println\("숫자를 입력하세요"\);

			x = import.nextInt\(\)

	\`\`\`



- 단축키 배웠는데 \(자동 정렬, 범위 지정해서 주석처리 하기\) 맥에서는 위 단축키가 안 먹는다. 주석처리는 cmd + /로 쓰고 있으니까 상관 없는데 자동 정렬이랑 expand, 키 이동 단축키는 알아놔야겠다. atom 처럼 못 쓰니까 불편하다. 



- 문제 풀기

	\`\`\`java

	import java.util.Scanner;



	public class Task0302 {



		public static void main\(String\[\] args\) {

			Scanner input = new Scanner\(System.in\);

			

			// 01. Input two numbers, then print a larger number.

			System.out.println\("01. Input two numbers, then print a larger number."\);

			

			int num1, num2;

			int compare;



			System.out.println\("Input a First Number : "\);

			num1 = input.nextInt\(\);

			System.out.println\("Input a Second Number : "\);

			num2 = input.nextInt\(\);

			

			compare = \(num1 &gt; num2\) ? num1 : num2;

			System.out.printf\("The largest number of %d, %d is %d. \n", num1, num2, compare\);



			

			// 02. Input three numbers, then print the largest number.

			System.out.println\("02. Input three numbers, then print the largest number"\);

			int x, y, z;

			int comp1, comp2;



			System.out.println\("Input a First Number : "\);

			x = input.nextInt\(\);

			System.out.println\("Input a Second Number : "\);

			y = input.nextInt\(\);

			System.out.println\("Input a Third Number : "\);

			z = input.nextInt\(\);

			

			comp1 = \(x &gt; y\) ? x : y;

			comp2 = \(comp1 &gt; z\) ? comp1 : z;

			System.out.printf\("The largest number of %d, %d, %d is %d.\n", x, y, z, comp2\);



			

			// 03. Input three numbers, then print the middle value.

			System.out.println\("03. Input three numbers, then print the middle value."\);

			int a, b, c;

			int result1, result2;



			System.out.println\("Input a First Number : "\);

			a = input.nextInt\(\);

			System.out.println\("Input a Second Number : "\);

			b = input.nextInt\(\);

			System.out.println\("Input a Third Number : "\);

			c = input.nextInt\(\);

			

			result1 = \(a &gt; b\) ? a : b;

			result2 = \(result1 &lt; c\) ? result1 : c;

			System.out.printf\("The middle value of %d, %d, %d is %d. \n", a, b, c, result2\);

			

			

			// 04. Input a score, then print the grade that matches these conditions.

			// Higher than 90 is A

			// Higher than 80 is B

			// Higher than 70 is C

			// Higher than 60 is D

			// Less than 60 is Idiot

			System.out.println\("04. Input a score, then print your grade."\);

			

			int score, result;

			String decision;

			

			System.out.println\("Input your score\(only number\) : "\);

			score = input.nextInt\(\);

			

			decision = \(score &lt; 60\)? "Idiot" : "D";

			decision = \(\(decision == "D"\) && score &gt;= 70\)? "C" : decision;

			decision = \(\(decision == "C"\) && \(score &gt;= 80\)\)? "B" : decision;		

			decision = \(\(decision == "B"\) && \(score &gt;= 90\)\)? "A" : decision;

			System.out.printf\("Your score is %d, so you got a\(an\) %s \n", score, decision\);

			

			//05. Input a 4-digits, then judge that number is leap year.

			System.out.println\("05. Input a 4-digits, then judge that number is leap year."\);

			

			int year;

			boolean decide;

			

			System.out.println\("Input a 4-digits\(year\): "\);

			year = input.nextInt\(\);

			

			decide = \(\(year % 4 == 0\) && \(year % 100 != 0\) \|\| \(year % 400 == 0\)\);

			System.out.printf\("result : %s", decide\);	



		}

	}

	\`\`\`

	- window에서 작성한 java파일을 mac에서 여니까 한글이 다 깨졌다. 협업할 때 등등 이런 문제가 또 생길 것 같은데 이를 예방하기 위해 취할 수 있는 조치를 알아놔야겠다. 참, 인코딩이 무엇인지도 수업때 잠시 들었는데 관련 내용 더 찾아봐야지 했었다. 

	- 윤년인지 판단

		- 논리연산자를 활용해 입력한 년도가 윤년에 조건에 맞는지 판단할 수 있다. 

		- 위의 문제를 푸는데 사용한 논리식을 집합 식으로 표현해보고 싶었는데 벤다이어그램으로 그리는건 쉬우나 집합 식으로 표현하는게 가물가물 했음.

		- !\[enter image description here\]\(https://lh3.googleusercontent.com/-OWaUT4LTv07EI-xrfQ58JMJljI\_r4u-rx8TERRxamKC9eOXeChc\_rlSPhSbOp-NgvKPvqeOu7s\)

			- 디지털 논리회로, 이산수학 교재를 훑어보니 여기서 이런 내용을 배울 수 있을 것 같다. &lt;로지코믹스&gt;와 &lt;수학자, 컴퓨터를 만들다&gt; 두 권의 책 덕분에 논리를 수학적으로 표현하는 방법에 관심이 생겼다. 

	- 시험 점수에 맞게 등급 출력

		- 삼항연산자를 활용해 입력받은 시험 점수가 어느 구간에 속하는지 판단할 수 있다.

		- if문 \(java로 아는 건 아니지만\)을 알고 있어서 이를 쓰지 않고 어떻게 이걸 만들 수 있을지 고민이 많이 되었다. 

		- 종이에 문제 풀이에 필요한 논리를 그려보는게 도움이 되었다. 

		- !\[enter image description here\]\(https://lh3.googleusercontent.com/LDl4pgfhZlDnIwL2FmwIylSoy-ac5pF-2D7R4bZk2m6UlXCFyWlfabWBXtbLktkUgfSowvX0Des\)

	- 두 개 중, 더 큰 숫자 출력

	- 세 개 중, 가장 큰 숫자 출력

	- 세 개 중, 중간 숫자 출력

		- 비교를 2번 해야 한다. 

		- 입력한 숫자의 개수가 변할 때, 크기를 비교하여 x번째 숫자를 출력할 수 있는 알고리즘은?



- 삼항연산자 

	- \`\(condition\)? exp1 : exp2;\` 조건문이 참이면 \`exp1\`실행, 조건문이 거짓이면 \`exp2\` 실행

	- 문제 풀면서, 특히 시험 점수에 맞게 등급 출력하는 것, if문이나 switch문을 삼항연산자를 활용해 표현할 수 있다는게 새로웠음. 이걸로도 충분하구나. 

- 논리연산자

	- \`&&\` AND 논리곱\(교집합\)

		- p, q가 각각 1로 같을 경우만 1

		- 주의 : p, q 각각 0으로 같으면 0이다. 

	- \`\|\|\` OR 논리합\(합집합\)

		- p, q 중 하나라도 1이 있으면 1

- 비교연산자

	- \`&gt;\` 크다 , \`&lt;\` 작다 , \`&gt;=\` 크거나 같다, \`&lt;=\` 작거나 같다 

	- \`==\` 같은지 비교, \`!=\` 같지 않은지 비교

- \`x++\` 과 \`++x\`의 차이

	- x++은 x 먼저 쓰고, x의 값 1 올리고, ++x는 먼저 올리고 x 쓴다. 

	- \`x++;\` 아래와 동일

		\`\`\`java

		System.out.println\(x\); 

		x = x+1;

		\`\`\`

	- \`++x;\` 아래와 동일

		\`\`\`java 

		x = x+1;

		System.out.println\(x\);

		\`\`\`  

	- 예시 문제

		\`\`\`java

		int x = 5; //x값 5

		++x; //x값 6

		System.out.println\(x++\); //x값 6출력 후, x값 7

		System.out.println\(x\); // 7출력

		--x; //x값 6

		System.out.println\(--x\); // x값 6에서 5로 줄이고 5출력

		\`\`\`

- 변수 선언/초기화

	- 변수는 이름\(name\)과 타입\(type\)으로 이루어져 있음. 

		- 이름은 말 그대로 변수의 이름, 중복되어서는 안 된다. \(고유해야 함. 왜냐하면 같은 이름이 여러개가 있으면 부르는게 이 변수인지 저 변수인지 알 수 없으므로 프로그램 실행할 수 없음\)

		- 타입은 데이터 유형을 말함. 메모리가 부족했을 때, 메모리 낭비를 최대한 줄이고 관리할 수 있도록 변수의 유형을 지정하여 사용했음.

		- 변수의 이름과 타입을 명시해 변수를 만드는 것을 변수를 선언한다고 하고, 선언한 변수에 대입 연산자\(=\)를 사용해 값을 대입하는 것을 변수를 초기화한다고 한다. 

			- \`int x = 10;\` 이처럼 변수의 선언과 초기화를 동시에 할 수 있다.



- 데이터 타입

	- 아직 다 배운건 아닌데, 이걸 제대로 모르니까 위에 문제 풀 때 연산으로 나온 결과랑 변수의 타입이 맞지 않아 오류를 뱉었다. 자바스크립트, 파이썬과 다르게 java는 변수의 타입을 미리 고민하여 적절히 사용하는게 중요한 것 같다. 

	- 기본 데이터 타입

		- 숫자형

			- \`int\` 정수형, 정수 범위 담을 수 있음

			- \`double\` 더블형, 정수보다 큰 범위 담을 수 있음

		- 문자형

			- \`char\` 한 문자만 저장 가능, 문자열 저장 불가능

		- 논리형

			- \`boolean\` True 또는 False 



\#\# 블랙홀

\*\*자바에서 주석 3가지

1. \`/\*내용\*/\` : 문단 주석

	- 이 주석은 /\*만 작성하면 이 이후 내용 다 주석처리 됨. 그리고 뒤에 내용 쓰는거 까먹어서 에러 발생 요인이 됨. 고로 // 쓰는 것을 추천

2. \`/\*\*내용 내용 내용\*/\` : 문서 주석

	- 전체적인 프로그램 개요 등, 문서화 시킬 때 사용 \(사용하는 상황이 좀 다름\)

3. \`//내용\` : 문장주석\*\*



\*\*변수 - 프로그램이 사용하는 데이터를 일시적으로 저장할 목적으로 사용하는 메모리 공간

직접적인 데이터를 뜻하는게 아니다\*\*



 \*\*변수는 프로그램이 실행되면서 영향을 받아 값이 바뀔 수 있는거고, 상수는 프로그램 실행되는동안 값이 바뀌지 않음\*\*



\*\*타입 - 이 변수 공간에 뭐가 들어올 수 있는지 정해주는 것

따듯한용 컵, 이라고 하나의 타입을 고정시켜준다. 

보드마카 펜 파란색 펜 - 빨간색 잉크 넣으면? 불량이다. 

-&gt; 오 이렇게 비유를 하니 재밌다. 또 '하나의 타입을 고정시켜준다'라는 개념. 기억해야 할 부분인 듯\*\*



\*\*메모리의 할당을 받는 행위를 변수의 선언이라고 한다.\*\* 



\*\*int x; 를 함으로 일어나는 일

메모리에 int 정수가 들어올 수 있는 x라는 이름의 공간을 메모리에 할당해줘, 라고 운영체제에 말 하는 것. 그럼 운영체제가 보고 오케이. 메모리에 x라는 공간을 만든다.\*\* 



안쓰는데 왜 만들까? 변수들

만들긴 만드는데 왜? 쓰지도 않는데

위에서 절차적으로 내려오니까 아래에서 쓰는지 안 쓰는지 모르니까 만든다.

마지막까지 절차지향적으로 내려오니까. 위에서는 아래에서 이게 쓸건지 안 쓸건지 어떻게 알아? 모르지.



!\[enter image description here\]\(https://photos-3.dropbox.com/t/2/AAA3Y\_amq0v2G6-Pm8pkvpGFKN6He-DVSW7NCer5Mvvzhg/12/875438832/png/32x32/1/\_/1/2/20180302111247.png/EKDQ87gJGKAMIAcoBw/R0sANL-1bh69RrK0\_t2HC3swP5TFqfqDaF\_B2x\_oaoQ?preserve\_transparency=1&size=800x600&size\_mode=3\)

100이라는 숫자를 그냥 만드는게 아님

상수 영역에 100이라는 숫자를 만들어야 함

그 다음 그 100이라는 숫자를 x에 집어 넣게 되는 것임

그 다음 200을 또 만들어서 y값에 집어 넣고

CPU가 x랑 y를 가져와서 더한다!

-&gt; 아하 CPU가 이럴 때 또 나오는구나



jvm 이 OS에 명령을 보내는데 cpu에 x랑 y 좀 더해줘

cpu가 x야!!! 부르면 메모리에서 쨘 하고 오고 \(아 부르는거 너무 귀여움 ㅋㅋㅋㅋ\)

y야!!! 하고 부르면 메모리에서 쨘 하고 오고

이 결과값 300은 상수를 거치지 않고 스택으로 바로 저장된다!

따라서 상수값에 300 저장되지 않는다!



!\[20180302124802.png\]\(https://photos-3.dropbox.com/t/2/AAAlAwHmpqNDsC0qvOLh644-AlBH8h29o1ktBXUYWt9M8Q/12/875438832/png/32x32/1/\_/1/2/20180302124802.png/EKDQ87gJGJEIIAcoBw/OQPfAiQZmJqLUDtFK84euqh1SLIRprNCUq7nBNNHVOs?preserve\_transparency=1&size=800x600&size\_mode=3\)



-&gt; 이 구조 꼭 이해하고 있어야 한다. 그래야 프로그래밍 할 수 있다!

콘솔에 20 입력하면 얘는 상수 거칠 필요 없이 바로 메모리 x로 들어갈 수 있음



!\[enter image description here\]\(https://photos-1.dropbox.com/t/2/AADDfXYSKC66AgCXzqLm6nKTaIcKb6f-1vr4kCg-V7-D9g/12/875438832/png/32x32/1/\_/1/2/20180302111800.png/EKDQ87gJGKAMIAcoBw/WWxZoAg398Wkze89mTzeJXI0xwnu\_pz72EJJ1mrbkFg?preserve\_transparency=1&size=800x600&size\_mode=3\)



메모리는 잠깐동안 가지고 있을 수 있는 공간

하드디스크에 있는 값을 CPU에 보내 연산하려고 하는데 하드 속도 너무 느려서 CPU 연산 속도 따라잡지 못함. 그래서 그 속도 단차 따라잡기 위해 메모리 생김. \(메모리도 CPU보다는 느림\) 



!\[enter image description here\]\(https://photos-5.dropbox.com/t/2/AAAAYbfjjllvcFJCIDcQGDemtElN45AG4vEoQcc9GcGCUw/12/875438832/png/32x32/1/\_/1/2/20180302114852.png/EKDQ87gJGKAMIAcoBw/SK9SISiRIowdATFkm\_dls3ChV1ZxsXnAt4XUvZrPXnA?preserve\_transparency=1&size=800x600&size\_mode=3\)



\`.\`은 접근연산자가 아니라 멤버 연산자로 부를 수 있는 듯

https://msdn.microsoft.com/ko-kr/library/b930c881.aspx



system이라는 얘기는 pc OS에서 모든 기능을 제공하는 애, 이 시스템의 표준, 가장 기초, 입력과 출력을 받을 수 있는 것, 운영체제 기능 빌려서 쓰는 것. 표준 입력과 출력에 대해서. 



!\[20180302115422.png\]\(https://photos-5.dropbox.com/t/2/AADEbBgrjHacSrHfBet29H55pDfb\_sf7-FYUw67ajMNbHQ/12/875438832/png/32x32/1/\_/1/2/20180302115422.png/EKDQ87gJGIIHIAcoBw/H2gMmwP7hGvyUrJF3odS2LK0jcxwGPXLbUW9KWwSmlw?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[enter image description here\]\(https://photos-2.dropbox.com/t/2/AADcZqFKRqpN9tG4XrH2dA8IdtAx2HiVXFxB3YXBFPhglQ/12/875438832/png/32x32/1/\_/1/2/20180302115751.png/EKDQ87gJGKAMIAcoBw/sDTsYcowgyfutc3bg8e89qpKJ4bt93ETq7Fh4GKaqJ0?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[enter image description here\]\(https://photos-1.dropbox.com/t/2/AAAviBWLhTSYndG3tehr90lBbou\_Ce5M2Al3OBabMULLmQ/12/875438832/png/32x32/1/\_/1/2/20180302115702.png/EKDQ87gJGKAMIAcoBw/Sgn24eL2m9wfKShTFrshSGDUY3uQ23d4nrgX13ykJMw?preserve\_transparency=1&size=800x600&size\_mode=3\)



System. 꾸러미는 필수적인 기능의 꾸러미. 그냥 언제든지 쓰고 싶을 때 쓸 수 있음.



Scanner 꾸러미는 외부에 있어서 import라는 놈을 선언해서 사용할 수 있음



!\[20180302120606.png\]\(https://photos-2.dropbox.com/t/2/AABytHWrD4PtdrnUf0k7Fgyr6IemvGMeLxORgAL\_g3thbA/12/875438832/png/32x32/1/\_/1/2/20180302120606.png/EKDQ87gJGKgHIAcoBw/cnBz620WEkQrH7HF-e587xYg3qKUy4Wq1V8GJ-n8TVg?preserve\_transparency=1&size=800x600&size\_mode=3\)



input!!!!하고 변수명 부르면 scanner가 뛰어 나옴 ㅋㅋㅋ

Scanner는 타입, input은 이름



문자랑 숫자를 같이 더하면 숫자가 문자가 되어서 더해짐. \(문자가 더 큰 범위이기 때문에\)

!\[20180302131010.png\]\(https://photos-6.dropbox.com/t/2/AAD5LUwFvQANjdvCeBHOn6cb\_aQUq6lMZnZVArPBPz73pQ/12/875438832/png/32x32/1/\_/1/2/20180302131010.png/EKDQ87gJGNQIIAcoBw/hjChTKbpWwwpJkfrnXNiDws8GFhXAV\_71FehyV0215c?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[enter image description here\]\(https://photos-3.dropbox.com/t/2/AAC\_tVm9K29KdXVIDXrfv23r9fwd5k--lLEYSO\_Ocf8nOQ/12/875438832/png/32x32/1/\_/1/2/20180302131320.png/EKDQ87gJGKAMIAcoBw/IkFd2Ag4agabAqkdAWUZLz7D3-vDFYQLhurwnGsk\_as?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[20180302131442.png\]\(https://photos-5.dropbox.com/t/2/AAA8tF0lriIn4I\_agXhXAyQbqZg4buU7vqEhFlIDGuRoJw/12/875438832/png/32x32/1/\_/1/2/20180302131442.png/EKDQ87gJGPMIIAcoBw/HGNyInYfcg8ogVdvi6L8IONyZhHN2LKlAvQu0hVKGAM?preserve\_transparency=1&size=800x600&size\_mode=3\)



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



!\[enter image description here\]\(https://photos-6.dropbox.com/t/2/AABq\_YB2RZTj652mj4m0jJdccPOAURzarvfpyPUGZaOvSQ/12/875438832/png/32x32/1/\_/1/2/20180302150021.png/EKDQ87gJGKAMIAcoBw/nNvZ5\_516Ldi1ddQfhdmxWolMovjdxD9SRJjdM8S968?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[enter image description here\]\(https://photos-6.dropbox.com/t/2/AABq\_YB2RZTj652mj4m0jJdccPOAURzarvfpyPUGZaOvSQ/12/875438832/png/32x32/1/\_/1/2/20180302150021.png/EKDQ87gJGKAMIAcoBw/nNvZ5\_516Ldi1ddQfhdmxWolMovjdxD9SRJjdM8S968?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[20180302151800.png\]\(https://photos-3.dropbox.com/t/2/AACaaUUGl\_-aAcJhPvUn-KAKh0LY4nWN\_5LBfuLHvYYqnw/12/875438832/png/32x32/1/\_/1/2/20180302151800.png/EKDQ87gJGNAJIAcoBw/GsYAduSqrUiiy4RR-gcjAUxzc8G7sazhyMJ8OyahOzU?preserve\_transparency=1&size=800x600&size\_mode=3\)



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



!\[enter image description here\]\(https://photos-3.dropbox.com/t/2/AAAMeGuUCNTLrSHolkhjnh43nGfLXiL85NxXzz7xyq7S2g/12/875438832/png/32x32/1/\_/1/2/20180302154058.png/EKDQ87gJGKAMIAcoBw/beePXc1akRie7roQI5aU7ZGjyeGfP2GeLDagrhTroj0?preserve\_transparency=1&size=800x600&size\_mode=3\)



이런이런 변수는 이런이름으로 할거야

설계하는 분이 보통 이런 변수들도 정리해서 주면 개발자가 바로 개발해서 사용할 수 있음

-&gt; 오오 디자인 리소스 이름 정하는게 이래서 또 중요하구나



!\[enter image description here\]\(https://photos-6.dropbox.com/t/2/AAD\_Fv8U5Qd3gRBNuzM-J1ldO3znj8JKVjhKz4JLir0iQg/12/875438832/png/32x32/1/\_/1/2/20180302154324.png/EKDQ87gJGKAMIAcoBw/Ch8qRWYEvkuSJ2qZYw-WWKTibG5cQS-Au8VHEXIzu94?preserve\_transparency=1&size=800x600&size\_mode=3\)



!\[enter image description here\]\(https://photos-6.dropbox.com/t/2/AAD\_Fv8U5Qd3gRBNuzM-J1ldO3znj8JKVjhKz4JLir0iQg/12/875438832/png/32x32/1/\_/1/2/20180302154324.png/EKDQ87gJGKAMIAcoBw/Ch8qRWYEvkuSJ2qZYw-WWKTibG5cQS-Au8VHEXIzu94?preserve\_transparency=1&size=800x600&size\_mode=3\)



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

그래서 이름이 단항 연산자구나 

두줄쓸거 한 번에 쓸 수 있다구 ㅋㅋ int nextX = ++x; 의미는 x = x+1; int nextX = x;



!\[enter image description here\]\(https://lh3.googleusercontent.com/OsAwCan2669OIIPr1ZeJMAaLsWJBl03IlY1XYSzNO9B6\_mwWcIMFfEeOu4zlh8VxAvLbjUwVe4Q\)



!\[20180302164207.png\]\(https://photos-1.dropbox.com/t/2/AAAkoOIq06y41mto7EKanUReaB9vGTNGRiN825zqqfwXlw/12/875438832/png/32x32/1/\_/1/2/20180302164252.png/EKDQ87gJGKAMIAcoBw/scaUxzzO4iiboX-Bm0lWN\_WWMim6wEJlGQ4xLKYODMg?preserve\_transparency=1&size=800x600&size\_mode=3\)



굉장히 중요!

관계연산의 결과물은 항상 boolean값으로 나옴



!\[enter image description here\]\(https://photos-6.dropbox.com/t/2/AABKsiBfR8CGTu3fljMpuGwg6\_WUqTEyYBBMDVSEVeSs\_w/12/875438832/png/32x32/1/\_/1/2/20180302164953.png/EKDQ87gJGKAMIAcoBw/kU2XwRarSZ2cYsHDdUEbN1BIoXuMFOAeIPxXuwUuiqk?preserve\_transparency=1&size=800x600&size\_mode=3\)





















\#\# 보충 학습

- \[ \] 인코딩이란?

&gt; 출처 : 출처: http://unikys.tistory.com/195 \[All-round programmer\]

&gt; 컴퓨터에서 인코딩\(Encoding\) 디코딩\(Decoding\)이란 말은 여러 가지 의미로서 사용됩니다. 그러나 어떤 경우든, 인코딩이란 정보를 부호화/암호화시킨다, 디코딩은 그 부호화/암호화를 해제한다는 뜻을 가집니다.

&gt; 

&gt; 텍스트 인코딩

&gt; 컴퓨터는 모든 글자에 하나씩 일련 번호를 매겨서 인식합니다. 이것을 인코딩\(Character Encoding\)이라고 합니다. 그런데 각 언어별로 번호 체계가 다릅니다. 가령 한글 윈도우의 메모장으로는 "한글 완성형 텍스트 파일"을 읽을 수 있습니다. 그러나 "일본어 Shift-JIS 텍스트"는 읽을 수가 없습니다. 메모장이 일본어 인코딩을 인식하지 못하기 때문입니다.

&gt;

&gt; 멀티미디어

&gt;가령 wav 또는 avi 파일을, 압축률이 높은 형식인 mp3 / mpg 등의 포맷으로 변환하는 작업을 인코딩이라고 합니다.



&gt; 인터넷 주소 \(URL\) 등에서 만약 이렇게 http://www.foo.com/신작 소설^^;.html 한글/공백/특수기호가 들어가면 문제가 생깁니다. 그래서 위의 주소를 다음과 같이 http://www.foo.com/%EC%8B%A0%EC%9E%91%20%EC%86%8C%EC%84%A4%5E%5E;.html

이렇게 바꾸는 작업을 또한 인코딩이라고 합니다.



위에도 그렇고, 아래 내용도 그렇고 URL 변환할 때도 이런 내용이 필요하구나. 



&gt; 출처 : http://unikys.tistory.com/195

&gt; \[자바\] String을 URL 인코딩하기

&gt; 

&gt; URL 뒤에 데이터를 덧붙이고자 할때 스트링을 URL에 맞게 인코딩을 해야하는데 아래와 같이 하면 된다.

&gt; String encodeResult = URLEncoder.encode\(String encodingString, String charsetName\);

&gt; 

&gt;그냥 URLEncoder.encode\(String s\); 는 deprecated 되었으니까 사용하지 말고 위의 함수를 사용하자.

charsetName에는 "UTF-8"과 같은 캐릭터 인코딩 셋을 넣으면 된다. 

&gt;

&gt; 반대로 디코딩하는 것은 아래와 같이 하면 된다.

&gt; 

&gt; String decodeResult = URLDecoder.decode\(String decodingString, String charsetName\);











