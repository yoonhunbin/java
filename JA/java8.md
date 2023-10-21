```
package homework;

import java.util.*;


public class Myprofile3 {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Random r = new Random();
		
		int num1[] = new int[2];
		num1[0] = 1;
		num1[1] = 2;
				
		while(true) {
			for(int i = 0; i < num1.length; i++) {
				if(num1[i] == 1) {
					System.out.println("내가 공을 찰 차례입니다.(키커)"
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
						}
						else System.out.println("골키퍼가 오른쪽으로 움직입니다.\n 골인입니다");
					}
					else if(choice1 == 2) {
						System.out.println("가운데로 공을 찼습니다.");
						if(GK == 1) {
							System.out.println("골키퍼가 왼쪽으로 움직입니다.\n 골인입니다.");
						}
						else if(GK == 2) {
							System.out.println("골키퍼가 가운데으로 움직입니다.\n 막았습니다.");
						}
						else System.out.println("골키퍼가 오른쪽으로 움직입니다.\n 골인입니다");
					}
					else if(choice1 == 3) {
						System.out.println("오른쪽으로 공을 찼습니다.");
						if(GK == 1) {
							System.out.println("골키퍼가 왼쪽으로 움직입니다.\n 골인입니다.");
						}
						else if(GK == 2) {
							System.out.println("골키퍼가 가운데으로 움직입니다.\n 골인입니다.");
						}
						else System.out.println("골키퍼가 오른쪽으로 움직입니다.\n 막았습니다.");
				}
					else if(choice1 == 4) {
						System.out.println("게임 끝");
						break;
					}
			}
				if(num1[i] == 2) {
					System.out.println("내가 공을 막을 차례입니다.(골키퍼)"
							+ "(왼쪽-1, 가운데-2, 오른쪽-3, 게임 끝-4)");
					int choice1 = s.nextInt();
					int GK = r.nextInt(3) + 1;
					
					if(choice1 == 1) {
						System.out.println("왼쪽으로 움직입니다.");
						if(GK == 1) {
							System.out.println("키커가 왼쪽으로 공을 찼습니다.\n 막았습니다.");
						}
						else if(GK == 2) {
							System.out.println("키커가 공을 가운데로 찼습니다.\n 골인입니다.");
						}
						else System.out.println("키커가 오른쪽으로 찼습니다.\n 골인입니다");
					}
					else if(choice1 == 2) {
						System.out.println("가운데로 움직입니다.");
						if(GK == 1) {
							System.out.println("키커가 왼쪽으로 찼습니다.\n 골인입니다.");
						}
						else if(GK == 2) {
							System.out.println("키커가 가운데로 찼습니다.\n 막았습니다.");
						}
						else System.out.println("키커가 오른쪽으로 찼습니다.\n 골인입니다");
					}
					else if(choice1 == 3) {
						System.out.println("오른쪽으로 움직입니다.");
						if(GK == 1) {
							System.out.println("키커가 왼쪽으로 찼습니다.\n 골인입니다.");
						}
						else if(GK == 2) {
							System.out.println("키커가 가운데로 찼습니다.\n 골인입니다.");
						}
						else System.out.println("키커가 오른쪽으로 찼습니다.\n 막았습니다.");
		}
					else if(choice1 == 4) {
						System.out.println("게임 끝");
					}
			
      }	
    }
   }
  }
}
```
