```
package homework;

import java.util.*;

public class Myprofile4 {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Random r = new Random();

		int me = 0;
		int cm = 0;

		int k = 1;

		while (k < 10) {
			if (k % 2 == 1) {
				System.out.println("내가 공을 찰 차례입니다.(키커)" + "(왼쪽-1, 가운데-2, 오른쪽-3, 게임 끝-4)");
				int player = s.nextInt();
				int computer = r.nextInt(3) + 1;

				if (player == 1) {
					System.out.println("왼쪽으로 공을 찼습니다.");
				} else if (player == 2) {
					System.out.println("가운데쪽으로 공을 찼습니다.");
				} else if (player == 3) {
					System.out.println("오른쪽으로 공을 찼습니다.");
				} else if (player == 4) {
					break;
				}

				if (computer == 1) {
					System.out.println("골키퍼가 왼쪽으로 공을 막았습니다.");
				} else if (computer == 2) {
					System.out.println("골키퍼가 가운데쪽으로 공을 막았습니다.");
				} else if (computer == 3) {
					System.out.println("골키퍼가 오른쪽으로 공을 막았습니다.");
				}

				if (computer != player) {
					// 공을 넣었을 때
					me += 1;
					System.out.println("골인입니다.");
				} else {
					// 공을 막힐 때
					System.out.println("막혔습니다.");
				}
			} else {
				System.out.println("내가 공을 막을 차례입니다.(골키퍼)" + "(왼쪽-1, 가운데-2, 오른쪽-3, 게임 끝-4)");
				int player = s.nextInt();
				int computer = r.nextInt(3) + 1;

				if (player == 1) {
					System.out.println("왼쪽으로 움직였습니다.");
				} else if (player == 2) {
					System.out.println("가운데로 움직였습니다.");
				} else if (player == 3) {
					System.out.println("오른쪽으로 움직였습니다.");
				} else if (player == 4) {
					break;
				}

				if (computer == 1) {
					System.out.println("왼쪽으로 공을 찼습니다.");
				} else if (computer == 2) {
					System.out.println("가운데로 공을 찼습니다.");
				} else if (computer == 3) {
					System.out.println("오른쪽으로 공을 찼습니다.");
				}
				if (computer != player) {
					// 공을 넣었을 때
					cm += 1;
					System.out.println("골인입니다.");
				} else {
					// 공을 막힐 때
					System.out.println("막혔습니다.");
				}
			}
			if (cm != me && k >= 10) {
				break;
			}
			k += 1;
		}
	}
}
```
