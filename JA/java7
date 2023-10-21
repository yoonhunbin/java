```
package homework;

import java.util.*;


public class Myprofile2 {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Random r = new Random();
		
		System.out.println("축구 게임을 시작합니다.");
		
		while(true) {
			System.out.println("내가 공을 찹니다. 어느 쪽으로 차겠습니까?"
					+ "(왼쪽-1, 가운데-2, 오른쪽-3, 게임 끝-4)");
			int choice1 = s.nextInt();
			int GK = r.nextInt(3) + 1;
			
			if(choice1 == 1) {
				System.out.println("왼쪽으로 공을 찼습니다.");
				if(GK == 1) {
					System.out.println("골키퍼가 왼쪽으로 움직입니다.\n 막았습니다.");
				}
				else if(GK == 2) {
					System.out.println("골키퍼가 가운데으로 움직입니다.\n 골인입니다.");
					break;
				}
				else System.out.println("골키퍼가 오른쪽으로 움직입니다.\n 골인입니다");
				break;
			}
			else if(choice1 == 2) {
				System.out.println("가운데로 공을 찼습니다.");
				if(GK == 1) {
					System.out.println("골키퍼가 왼쪽으로 움직입니다.\n 골인입니다.");
					break;
				}
				else if(GK == 2) {
					System.out.println("골키퍼가 가운데으로 움직입니다.\n 막았습니다.");
				}
				else System.out.println("골키퍼가 오른쪽으로 움직입니다.\n 골인입니다");
				break;
			}
			else if(choice1 == 3) {
				System.out.println("오른쪽으로 공을 찼습니다.");
				if(GK == 1) {
					System.out.println("골키퍼가 왼쪽으로 움직입니다.\n 골인입니다.");
					break;
				}
				else if(GK == 2) {
					System.out.println("골키퍼가 가운데으로 움직입니다.\n 골인입니다.");
					break;
				}
				else System.out.println("골키퍼가 오른쪽으로 움직입니다.\n 막았습니다.");
			}
			else if(choice1 == 4) {
				System.out.println("게임 끝.");
				break;
			}
		}
	}	
}
```
