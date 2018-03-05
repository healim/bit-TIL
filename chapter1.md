# Day003

제어문 = 선택문이라고도 함

if\(만약~라면\)는 단독 사용 가능, else\(그밖에\)는 불가능

문장 한 줄만 있는게 단일문장

단일문장

복합문

\`\`\`java

if \(조건문\)

실행문

    


if \(조건문\) {

//{} 중괄호로 블록 설정, 단일문 대신 들어갈 수 있음

실행문1

실행문1

}

\`\`\`

\`\`\`java

if \(condition\)

exp1 //원래 이렇게 줄 띠고 쓰면 if가 아니라 그냥 실행문으로 판단되었는데 업데이트 되어서인지 if 뒤에 바로 안 붙여도 if에 붙은걸로 판단된다는

\`\`\`

![](https://lh4.googleusercontent.com/3HeJvNjP0f0wtRMnLsr4a155T67VenHER_ttL7-o-8Lz6sef30OJsy1EXWn5X8dNZ_QRlnkosma2jZ4iXITCwhXWHoX7gz_DNO0kSfqhVGEYoPC5ktjJzT5OoYZaNbuC_x7GCuIM)

    


메모리 어떤 식으로 동작해서 계산 되는가, 컴파일 과정

if 조건문 안 맞으면 바로 {} 브라켓 밖으로 이동함 \(체크표시 된 곳, 10번 라인 \*11번 라인이 아니다\*\)

현재 스코어 몇이냐~ cpu가 물어봄

메모리에 담긴 score값 83 가져와서 if 조건문에 집어 넣음, 판단해보니 결과값 False값 나옴

모든 조건문은 결과값 반드시 True 또는 False로 나오게 됨

if - else로 썼는데, 위에 사진처럼 if - if 로도 쓸 수 있지!

    


 코드 중첩 - 연속적인 if 문

```java
import java.util.Scanner;

public class Q1 {

	public static void main(String[] args) {
		int score;
		
		Scanner input = new Scanner(System.in);
		System.out.println("점수를 입력하세요");
		score = input.nextInt();
		
//		if (score >= 90){
//			System.out.println("A");
//		}
//		else if (score >= 80) {
//			System.out.println("B"); //실행문이 1개일때라 중괄호 쓰지 않아도 되는구나. 
//		}
//		else if ( score >= 70) {
//			System.out.println("C");
//		}
//		else if (score >= 60){
//			System.out.println("D");
//		}
//		else {
//			System.out.println("바보");
//		}
		
		if (score >= 90){
			System.out.println("A");
		}
		if (score < 90 && score >= 80){ // 이런 식으로 쓰려면 그냥 score >= 80만 쓰면 안 되고, score < 90 이런 식으로 써야 되는구나.
			System.out.println("B");
		}
		if (score < 80 && score >=70) {
			System.out.println("C");
		}
		if (score <70 && score >= 60){
			System.out.println("D");
		}
		if (score < 60) {
			System.out.println("바보");
		}

	}
}
```

  

```java
//중첩 지저분 
if (score >= 90){
			System.out.println("A");
		}
		else {
			if (score >= 80) {
				System.out.println("B");
			}
			else {
				if (score >= 70);
					System.out.println("C");
			}
		}

```

![](/assets/import.png)

```java

public class ifDiceEx {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int num = (int)(Math.random()*6) + 1; //1부터 6까지 난수 생성
		
		if (num == 1)
			System.out.printf("%d, 1이 나왔음 \n", num);
		else if (num == 2)
			System.out.printf("%d, 2가 나왔음 \n", num);
		else if (num == 3)
			System.out.printf("%d, 3이 나왔음 \n", num);
		else if (num == 4)
			System.out.printf("%d, 4가 나왔음 \n", num);
		else if (num == 5)
			System.out.printf("%d, 5가 나왔음 \n", num);
		else if (num == 6)
			System.out.printf("%d, 6이 나왔음 \n", num);

	}
	
	//if (num == [조사 '이'랑 쓰는 숫자 1, 3, 6])
	//	System.out.printf("%d이 나왔음 \n", num);
	//else (num == [조사 '가'랑 쓰는 숫자 2, 4, 5]
	// 	System.out.printf("%d가 나왔음 \n", num);
	// 집합 안에 있는 원소 중에 하나랑 맞는지 비교하려면 어떻게 해야하지?
	// 

}
```



이 거 생각하니까 홍길동 '님' 은 어쩌구... 이름뒤에 '님' 쓰면 은/는/이/가 구분할 필요가 없어지는구나.

기능 설계 잘 해서 개발이 편해질수도 있네! 예전에 if 배운 뒤 이름 입력 받아서 랜덤 전생? 알려주는 심리테스트 비슷하게 만들어보려 했음. 예를 들어, 이름이 홍길동이면 홍길동의 전생은



switch \(변수\) if 처럼 조건이 아니라 변수로 비교함![](/assets/import2.png)

```java
import java.util.Scanner;

public class SwitchEx {

	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		
		int number;
		
		System.out.println("숫자를 입력하시오:");
		number = input.nextInt();
		
		switch (number) {
		case 0:
			System.out.println("없음");
		case 1:
			System.out.println("하나");
		case 2:
			System.out.println("둘");
			break;
		default:
			System.out.println("없음");
			break;
			
		}

	}

}
```

**위 코드에 0을 입력하면 실행 결과가 어떻게 나올까?**

없음 하나 둘 //없음만 나오는 줄 알았는데, 없음 하나 둘이구나. break가 없어서 절차지향 쭉쭉 내려오면서 다 실행 됨

3 집어 넣으면?

많음 \(걸리는게 없으니까 위에는 안 걸치고 바로 default로 감\)







