가위바위보 5판3선승제
```java
package homework;

import java.util.*;

public class Myprofile4 {
	public static void main(String[] args) {
		Random r = new Random();
    Scaaner s = new Scanner(System.in);
      
		int mywin = 0;
		int comwin = 0;
		int draw = 0;
	
		for(int i = 0; i < 5; i++) {
		System.out.println("가위(1), 바위(2), 보(3), 중지(4)");
		int me = s.nextInt();
		int com = r.nextInt(3)+1;
		
		if ((me == 1) && (com == 1)) {
			System.out.println("나: 가위, 컴: 가위 비겼습니다.");
			draw = draw + 1;
		}
		else if ((me == 1) && (com == 2)) {
			System.out.println("나: 가위, 컴: 바위 컴퓨터가 이겼습니다.");
			comwin = comwin + 1;
		}
		else if ((me == 1) && (com == 3)) {
			System.out.println("나: 가위, 컴: 보 사용자가 이겼습니다.");
			mywin = mywin + 1;
		}
		else if ((me == 2) && (com == 2)) {
			System.out.println("나: 바위, 컴: 바위 비겼습니다.");
			draw = draw + 1;
		}
		else if ((me == 2) && (com == 1)) {
			System.out.println("나: 바위, 컴: 가위 사용자가 이겼습니다.");
			mywin = mywin + 1;
		}
		else if ((me == 2) && (com == 3)) {
			System.out.println("나: 바위, 컴: 보 컴퓨터가 이겼습니다.");
			comwin = comwin + 1;
		}
		else if ((me == 3) && (com == 3)) {
			System.out.println("나: 보, 컴: 보 비겼습니다.");
			draw = draw + 1;
		}
		else if ((me == 3) && (com == 1)) {
			System.out.println("나: 보, 컴: 가위 컴퓨터가 이겼습니다.");
			comwin = comwin + 1;
		}
		else if ((me == 3) && (com == 2)) {
			System.out.println("나: 보, 컴: 바위 사용자가 이겼습니다.");
			mywin = mywin + 1;
		}
		if ((mywin == 3) || (comwin == 3)) {
			break;
		}
		if (me == 4) {
			System.out.println("중지");
			break;
		}
		}
	System.out.println("사용자 윈: " + mywin + "," + "컴퓨터 윈: " + comwin + "," + "비김: " + draw);
	
	}
    } 
```
격투게임 무조건 1명이상 쓰러져야함
```java
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile5 {
	public static void main(String[] args) {
		int wizardH = 100;
		int warriorH = 200;

		Random random = new Random();

		Scanner scanner = new Scanner(System.in);

		while(wizardH > 0 && warriorH > 0) {
			System.out.print("공격하려면 1을 누르세요. 외 숫자를 입력하면 종료합니다.");
			int choice = scanner.nextInt();

			if (choice == 1) {
				int wizardD = random.nextInt(11) + 15;
				int warriorD = random.nextInt(11) + 5;

				warriorH = warriorH - wizardD;
				wizardH = wizardH - warriorD;

				System.out.println("마법사 HP: " + wizardH + ", 전사 HP: " + warriorH);
				if (warriorH <= 0 && wizardH <= 0) {
					System.out.println("마법사와 전사가 동시에 죽었습니다.");
					break;
				}

				else if (warriorH <= 0) {
					System.out.println("마법사가 이겼습니다. 전사가 죽었습니다.");
					break;
				}

				else if (wizardH <= 0) {
					System.out.println("전사가 이겼습니다. 마법사가 죽었습니다.");
					break;
				}
		}
		}
		System.out.println("종료합니다");
		}
}
```
좀비탈출게임
```java
age homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile6 {
	public static void main(String[] args) {
		Random r1 = new Random();
		Scanner s = new Scanner(System.in);

		int Choice1 = r1.nextInt(3) + 1;
		
		int player = 1;
			
		int zom1 = 7, zom2 = 15;

		while(true) {
			System.out.println("1(왼쪽), 2(오른쪽), 3(점프).");
			int Choice2 = s.nextInt();
	
			if (Choice2 == 1) {
				player -= 1;
				if(player <= 0) player = 1;
				System.out.println("왼쪽으로 움직였습니다. 현재 위치는" + player + "입니다.");
			} else if (Choice2 == 2) {
				player += 1;
				System.out.println("오른쪽으로 움직였습니다. 현재 위치는" + player + "입니다.");
			} else if (Choice2 == 3){
				player += Choice1;
				System.out.println("점프했습니다.현재 위치는" + player + "입니다.");
			}
			
			zom1 = zom1 + r1.nextInt(3) - 1;
			zom2 = zom2 +r1.nextInt(3) - 1;
			if (zom1 >= 20) {
				zom1 = 20;
			}
			if (zom1 <= 0) {
				zom1 = 1;
			}
			if (zom2 >= 20) {
				zom2 = 20;
			}
			if (zom2 <= 0) {
				zom2 = 1;
			}
			System.out.println("좀비1의 좌표:" + zom1 + "좀비2의 좌표" + zom2);
			
			if (player == zom1 || player == zom2) {
				System.out.println("좀비에게 잡혔습니다. 처음위치에서 다시 시작합니다.");
				player = 1; zom1 = 7; zom2 = 15;
			}
			if (player >= 20) {
				System.out.println("미션 클리어 목적지에 도착했습니다.");
				break;
			}
		}
	}
}
```
while문 활용



