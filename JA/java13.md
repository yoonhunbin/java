<h1>좀비게임 좀비 class</h1>
```
package zom;

import java.util.Random;

public class zoms {
	Random r = new Random();
	String name;
	int pos;
	
	public zoms(String n , int p) {
		name = n;
		pos = p;
	}
	
	public void move() {
		pos = pos + r.nextInt(3) - 1;
		System.out.println(name + "의 현재위치는" + pos + "입니다.");
	}

}
```
