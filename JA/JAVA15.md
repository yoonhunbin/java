<h1>좀비게임 게임 class</h1>
```
package zom;

import java.util.Scanner;

public class zombiGame {
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		zoms zom1 = new zoms("좀비1", 7);
		zoms zom2 = new zoms("좀비2", 15);
		RaLo ralo = new RaLo("랄로", 1, 3);
		
		while(true) {
			System.out.println("왼쪽(1), 오른쪽(2), 점프(3)");
			int input = s.nextInt();
			if(input == 1) ralo.leftMove();
			else if(input == 2) ralo.rightMove();
			else if(input == 3) ralo.jump();
			
			zom1.move();
			zom2.move();
			
			if((ralo.pos == zom1.pos) || (ralo.pos == zom2.pos)) {
				ralo.life--;
				int c = ralo.life;
				System.out.println("현재 라이프" + c);
			}
			if(ralo.life == 0) {
				System.out.println("죽으셨습니다.");
				break;
			}
			if(ralo.pos < 0) {
				ralo.pos = 0;
			}
			if(ralo.pos >= 20) {
				System.out.println("탈출하셨습니다.");
				break;
			}
		}
	}
}
```
