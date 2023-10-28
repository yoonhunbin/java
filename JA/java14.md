<h1>좀비게임 인간 class</h1>
```
package zom;

import java.util.Random;

public class RaLo {
	Random r = new Random();
	String name;
	int pos;
	int life;
	
	public RaLo(String n, int p, int l) {
		name = n;
		pos = p;
		life = l;
	}
	public void leftMove() {
		pos = pos - 1;
		System.out.println(name + "이 왼쪽으로 이동하여 현재위치는" + pos + "입니다.");
	}
	public void rightMove() {
		pos = pos + 1;
		System.out.println(name + "이 오른쪽으로 이동하여 현재위치는" + pos + "입니다.");
	}
	public void jump() {
		int a = r.nextInt(3) + 1;
		pos = pos + a;
		System.out.println(name + "이" + a + "만큼 점프했습니다." + "현재위치는" + pos + "입니다.");
	}
}
```
