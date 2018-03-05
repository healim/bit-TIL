# Day003

제어문 = 선택문이라고도 함

if\(만약~라면\)는 단독 사용 가능, else\(그밖에\)는 불가능

문장 한 줄만 있는게 단일문장

단일문장

복합문

```java
if (조건문)
    실행문

if (조건문) {
//{} 중괄호로 블록 설정, 단일문 대신 들어갈 수 있음
    실행문1
    실행문2
}


if (condition)

    exp1 
//원래 이렇게 줄 띠고 쓰면 if가 아니라 그냥 실행문으로 판단되었는데 업데이트 되어서인지 if 뒤에 바로 안 붙여도 if에 붙은걸로 판단된다는
```

![](https://lh4.googleusercontent.com/3HeJvNjP0f0wtRMnLsr4a155T67VenHER_ttL7-o-8Lz6sef30OJsy1EXWn5X8dNZ_QRlnkosma2jZ4iXITCwhXWHoX7gz_DNO0kSfqhVGEYoPC5ktjJzT5OoYZaNbuC_x7GCuIM)

메모리 어떤 식으로 동작해서 계산 되는가, 컴파일 과정

if 조건문 안 맞으면 바로 {} 브라켓 밖으로 이동함 \(체크표시 된 곳, 10번 라인 \*11번 라인이 아니다\*\)

현재 스코어 몇이냐~ cpu가 물어봄

메모리에 담긴 score값 83 가져와서 if 조건문에 집어 넣음, 판단해보니 결과값 False값 나옴

모든 조건문은 결과값 반드시 True 또는 False로 나오게 됨

**if - else로 썼는데, 위에 사진처럼 if - if 로도 쓸 수 있지! 이거 차이 **

코드 중첩 - 연속적인 if 문

```java
import java.util.Scanner;

public class Q1 {

    public static void main(String[] args) {
        int score;

        Scanner input = new Scanner(System.in);
        System.out.println("점수를 입력하세요");
        score = input.nextInt();

//        if (score >= 90){
//            System.out.println("A");
//        }
//        else if (score >= 80) {
//            System.out.println("B"); //실행문이 1개일때라 중괄호 쓰지 않아도 되는구나. 
//        }
//        else if ( score >= 70) {
//            System.out.println("C");
//        }
//        else if (score >= 60){
//            System.out.println("D");
//        }
//        else {
//            System.out.println("바보");
//        }

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
    //    System.out.printf("%d이 나왔음 \n", num);
    //else (num == [조사 '가'랑 쓰는 숫자 2, 4, 5]
    //     System.out.printf("%d가 나왔음 \n", num);
    // 집합 안에 있는 원소 중에 하나랑 맞는지 비교하려면 어떻게 해야하지?
    // 

}
```

이 거 생각하니까 홍길동 '님' 은 어쩌구... 이름뒤에 '님' 쓰면 은/는/이/가 구분할 필요가 없어지는구나.

기능 설계 잘 해서 개발이 편해질수도 있네! 예전에 if 배운 뒤 이름 입력 받아서 랜덤 전생? 알려주는 심리테스트 비슷하게 만들어보려 했음. 예를 들어, 이름이 홍길동이면 홍길동은 과거에 ㅇㅇ 이었다. 같이. 근데  이거 하려니까 이름마다 조사가 달라서 홍길동는 처럼 부자연스러운 문장들이 생겼음. 그렇다고 이걸 이름 마지막 글자에 따라서 이름의 마지막 글자 추출하고 case문으로 다 구분할수도 없고...  그래서 그런건 어떻게 구현하는거지? 고민했음

**switch \(변수\) if 처럼 조건이 아니라 변수로 비교함**![](/assets/import2.png)

![](/assets/import2.png)

![](/assets/import2.png)

![](/assets/import2.png)

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

if 대신 switch 쓰기

```java
import java.util.Scanner;

public class SwitchEx {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int number;
        int numberCond;

        System.out.println("정수를 입력하시오:");
        number = input.nextInt();
        numberCond = number / 100; 

        switch (numberCond) {
        case 0:
            System.out.println("미꾸스몰");
            break;
        case 1:
            System.out.println("미꾸미디움");
            break;
//        case 2: //이 케이스 굳이 없어도 되는데 있는게 명시적인듯
//            System.out.println("미꾸라지");
//            break;
//    
        default:
            System.out.println("미꾸라지");
            break;

        }

    }

}
```

```java
import java.util.Scanner;

public class SwitchEx {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        //문1.
        int number;

        System.out.println("1부터 10사이의 수를 입력하세요.: ");
        number = input.nextInt();

        // 문1-1. Switch 문으로 구현하기
        switch (number) {
        case 1:
            System.out.println("Bananas");
            break;
        case 2:
            System.out.println("Oranges");
            break;
        case 3:
            System.out.println("Pears");
        case 4:
            System.out.println("Apples");
        case 5:
            System.out.println("Plums");
            break;
        case 6:
            System.out.println("Pineapples");
            break;
        case 7:
            break;
        default:
            System.out.println("Nuts");
            break;

        }

        // 문1-2. If문으로 구현하기
        if (number <= 1 && number > 0)
            System.out.println("Bananas");
        else if (number <= 2)
            System.out.println("Oranges");
        else if (number <= 3){
            System.out.println("Pears \nApples \nPlums");
        }
        else if (number <= 4){
            System.out.println("Apples \nPlums");
        }
        else if (number <= 5)
            System.out.println("Plums");
        else if (number <= 6)
            System.out.println("Pineapples");
        else if (number <= 7 && number < 8)
            System.out.println("");
        else
            System.out.println("Nuts");


        //문2. 난수 생성기 사용
        int ranNum = (int)(Math.random()*10)+1;
        System.out.printf("생성된 난수 : %d \n", ranNum);

        // 문2-1. Switch 문으로 구현하기
        switch (ranNum) {
        case 1:
            System.out.println("Bananas");
            break;
        case 2:
            System.out.println("Oranges");
            break;
        case 3:
            System.out.println("Pears");
        case 4:
            System.out.println("Apples");
        case 5:
            System.out.println("Plums");
            break;
        case 6:
            System.out.println("Pineapples");
            break;
        case 7:
            break;
        default:
            System.out.println("Nuts");
            break;

        }

        // 문2-2. If문으로 구현하기
        if (ranNum <= 1 && ranNum > 0)
            System.out.println("Bananas");
        else if (ranNum <= 2)
            System.out.println("Oranges");
        else if (ranNum <= 3){
            System.out.println("Pears \nApples \nPlums");
        }
        else if (ranNum <= 4){
            System.out.println("Apples \nPlums");
        }
        else if (ranNum <= 5)
            System.out.println("Plums");
        else if (ranNum <= 6)
            System.out.println("Pineapples");
        else if (ranNum <= 7 && ranNum < 8)
            System.out.println("");
        else
            System.out.println("Nuts");



    }

}
```

형변환 `(double)(Math.random())`

정수 2개와 연산 기호 입력 받아서 사칙연산 수행하는 코드 만들어보는데 java에서는 if문 조건안에 문자비교 못 한다고 한다. 그래서 다른 방법 써야 한다고! 근데 js는 문자비교 되었던 것 같아서 해봤더니 된다.

```js
x = "+"

if(x == "+"){
  console.log("Success"); //console에 "Success" 출력됨
}
```

```java
//사칙연산 하는 프로그램

import java.util.*;

public class Ex0303 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        double x, y; //나누기 생각 못하고 처음에 int로 선언했다가, double로 바꿨다. 
        String cal;

        System.out.println("첫번째 정수를 입력하세요");
        x = input.nextDouble(); //double 자료형 콘솔에서 입력 받으려면 nextDouble()사용 

        System.out.println("두번째 정수를 입력하세요");
        y = input.nextDouble();

        System.out.println("처리할 연산을 입력하세요");
        cal = input.next();
        //위 코드 input.nextLine(); 으로 치니까 연산 문자 입력하는거 안 기다리고 '계산할 수 없습니다' 출력됨
        // 


        //if문은 == 문자 비교 안 된다 (그래서 다른 방식 써야 한다)
        switch(cal){
            case "+":
                System.out.println(x+y);
                break;
            case "-":
                System.out.println(x-y);
                break;
            case "*":
                System.out.println(x*y);
                break;
            case "/":
                System.out.println(Math.round(x/y)); //반올림은 어떻게하지? 그냥 Math.round()쓰니까 정수로 변환되는데
                break;
            default:
                System.out.println("계산할 수 없습니다.");
                break;

        }


    }

}
```

* 자료형 보충 \(문제 풀고 시간이 좀 남아서 자습...\)

  * 자료형, 연산자들 뭐뭐 있는지 제대로 모른다.

    * 자료형 생각하니까 전에 c 보면서 c는 int 자료형이 \(컴퓨터에 따라서\) 32비트 또는 64비트로 나뉜다고 내용 봤던 것 같은데 java는 jvm으로 OS 상관없이 돌아가니까? int 크기 통일인가?

      * 아 다 다르구나, 언어 - 컴파일이 정의하기 나름이라고?

      > No,`int`in C is**not**defined to be 32 bits.`int`and`long`are not defined to be any specific size at all. The only thing the language guarantees is that`sizeof(char)<=sizeof(short)<=sizeof(long)`.
      >
      > Theoretically a compiler could make`short`,`char`, and`long`all the same number of bits. I know of some that[actually did that](https://en.wikipedia.org/wiki/64-bit_computing#64-bit_data_models)for all those types save`char`.
      >
      > This is why C now defines types like`uint16_t`and`uint32_t`. If you need a specific size, you are supposed to use one of those.

      [https://stackoverflow.com/questions/6155784/range-of-values-in-c-int-and-long-32-64-bits](https://stackoverflow.com/questions/6155784/range-of-values-in-c-int-and-long-32-64-bits)

      * 그럼 c, java, c++ ? 데이터 타입있는 언어들은 다 각기 다른가?

      * 읽어보기

        * [Java Primitive Data Types. Size, Range and Default Value of Basic Data Types](http://cs-fundamentals.com/java-programming/java-primitive-data-types.php)

반복문

**if문이랑 while문 구조 비교**해볼 수 있구나, 공통점과 차이점

펜이랑 종이로 돌아가는 순서 꼭꼭 그려보기! \(메모리\)

```java
public class WhileEx {
    public static void main(String[] args){
        int i = 0;
        while (i < 5){
            System.out.println("정수: " + i);
            ++i;
        }
    }
}
```

위 코드 손으로 그려서 실행 순서 설명해보기

while문은 false 나올 때까지 돌리게 됨 ㄷㄷ

```java
public class WhileEx {
    public static void main(String[] args){
        int i = 3;
        while (i < 5){ //while 자리에 if도 써보자
            System.out.println("5보다 작네? ㅋㅋ");
            //한번 출력하고 종료되는 줄 알았더니, 종료 조건이 없으므로 무한 반복이 되는구나.

        }
    }
}
```

![](/assets/import3.png)![](/assets/day003import.png)

while에서는** 반복계수** 중요중요

