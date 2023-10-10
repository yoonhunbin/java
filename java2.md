홀 짝 맞추기
```java
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile {
	public static void main(String[] args) {
		Random r1 = new Random();

        int dice1 = r1.nextInt(6) + 1;

        Scanner s1 = new Scanner(System.in);

        System.out.print("홀(1) 또는 짝(2)을 입력하세요: ");
        int Choice = s1.nextInt();

        System.out.println("컴퓨터의 주사위 값: " + dice1);
        

        if (dice1 % 2 == 0 && Choice == 2) {
            System.out.println("축하합니다! 사용자가 이겼습니다.");
        }else if (dice1 % 2 != 0 && Choice == 1) {
        	System.out.println("축하합니다! 사용자가 이겼습니다.");
        }else {
        	System.out.println("컴퓨터가 이겼습니다. 다음 기회에 다시 시도하세요.");
        }
        
        s1.close();
    }	
	}
```
캐릭터 움직이기
```java
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile4 {
	public static void main(String[] args) {
		Random r1 = new Random();
		Scanner s = new Scanner(System.in);

		int Choice1 = r1.nextInt(3) + 1;

		System.out.println("1(왼쪽), 2(오른쪽), 3(점프) 숫자를 입력하세요.");
		int Choice2 = s.nextInt();

		int num1 = 1;

		if (Choice2 == 1) {
			num1 -= 1;
			System.out.println("왼쪽으로 움직였습니다. 현재 위치는" + num1 + "입니다.");
		} else if (Choice2 == 2) {
			num1 += 1;
			System.out.println("오른쪽으로 움직였습니다. 현재 위치는" + num1 + "입니다.");
		} else {
			num1 += Choice1;
			System.out.println("점프했습니다.현재 위치는" + num1 + "입니다.");
		}
	}
}
```
