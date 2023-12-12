<h1>배열 연습</h1>

1번쨰
```
package homework;

import java.util.*;


public class Myprofile {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Random r = new Random();
		int intArray [] = new int[5];
		int max = 0;
		
		System.out.println("가장 큰 수를 입력하세요");
		for (int i = 0;i < 5; i++) {
			intArray[i] = r.nextInt(100)+1;
			if(intArray[i] > max) {
				max = intArray[i];
			}
		System.out.println("가장 큰 수는" + max + "입니다.");	
		}
    }	
}
```
2번쨰
```
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile2 {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		
		int map[] = new int[30];

		int pos = 0;
		
		map[pos] = 0;
		
		while(true) {
			for(int i = 0; i < map.length; i++) {
				System.out.print(map[i]);
			}
			System.out.println();
			System.out.println("왼쪽(1), 오른쪽(2)");
			int input = s.nextInt();
			
			if(input == 1) {
				map[pos] = 0;
				pos--;
				if(pos<=0) {
					pos = 0;
					System.out.println("맵 밖으로 나갈 수 없습니다");
				}
				else map[pos] = 1;
			}
			else if(input == 2) {
				map[pos] = 0;
				pos++;
				map[pos] = 1;
			}
			else System.out.println("잘못입력했습니다.");
			
			if(pos == 29) System.out.println("맵 목적지에 도착했습니다.");
			break;
		}
	}
}
```
3번쨰
```
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile3 {
	public static void main(String[] args) {
		Random r1 = new Random();
		Scanner s = new Scanner(System.in);
		
		System.out.println("입력할 학생 수를 입렵하세요.");
		int num = s.nextInt();
		
		int korean[] = new int[num];
		int English[] = new int[num];
		int math[] = new int[num];
		int sum[] = new int[num];
		double avg[] = new double[num];
		
		for(int i = 0; i < num; i++) {
			System.out.println("국어, 영어, 수학 성적을 입력하세요.");
			korean[i] = s.nextInt();
			English[i] = s.nextInt();
			math[i] = s.nextInt();
			sum[i] =  korean[i] + English[i] + math[i];
			avg[i] = sum[i] / 3.0;
		}
		for(int i = 0; i < num; i++) {
			System.out.println(i+"번 학생의 성적 평균은" + avg[i]);
		}
	}
}
```
4번쨰
```
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile4 {
	public static void main(String[] args) {
		Random r1 = new Random();
		Scanner s = new Scanner(System.in);
		
		System.out.println("입력할 학생 수를 입렵하세요.");
		int num = s.nextInt();
		int data[][] = new int[num][4];
		
		for(int i = 0; i < num; i++) {
			System.out.println("국어, 영어, 수학 성적을 입력하세요.");
			for(int j = 0; j < 3; j++) {
				data[i][j] = s.nextInt();
			}
			data[i][3] = data[i][0] + data[i][1] + data[i][2];
		}
		
		int korean[] = new int[num];
		int English[] = new int[num];
		int math[] = new int[num];
		int sum[] = new int[num];
		double avg[] = new double[num];
		
		for(int i = 0; i < num; i++) {
			System.out.println("국어, 영어, 수학 성적을 입력하세요.");
			korean[i] = s.nextInt();
			English[i] = s.nextInt();
			math[i] = s.nextInt();
			sum[i] =  korean[i] + English[i] + math[i];
			avg[i] = sum[i] / 3.0;
		}
		for(int i = 0; i < num; i++) {
			System.out.println(i+"번 학생의 성적 평균은" + avg[i]);
		}
	}
}
```
5번쨰
```
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile5 {
	public static void main(String[] args) {
		Random r1 = new Random();
		Scanner s = new Scanner(System.in);

		int Choice1 = r1.nextInt(3) + 1;
		
		int player = 1;
		
		int zoms[] = new int[2];
		
		zoms[0] = 7;
		zoms[1] = 15;
		
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
			} else if ((Choice2 < 1) || (Choice2 > 3)) {
				System.out.println("잘못입력했습니다.");
				break;
			}
			for(int b = 0; b < zoms.length; b++) {
				zoms[b] = zoms[b] + r1.nextInt(3) - 1;
				System.out.println("좀비" + (b + 1) + "의 좌표: " + zoms[b] + " ");
			}if (zoms[0] >= 20) {
				zoms[0] = 20;
			}if (zoms[0] <= 0) {
				zoms[0] = 1;
			}if (zoms[1] >= 20) {
				zoms[1] = 20;
			}if (zoms[1] <= 0) {
				zoms[1] = 1;
			}
			
			for (int c = 0; c < zoms.length; c++) {
				if(player == zoms[c]) {
					System.out.println("좀비에게 잡혔습니다. 처음위치에서 다시 시작합니다.");
      				player = 1; zoms[0] = 7; zoms[1] = 15;
				}
			}
			if (player >= 20) {
				System.out.println("미션 클리어 목적지에 도착했습니다.");
				break;
			}
		}
	}
 }
```
