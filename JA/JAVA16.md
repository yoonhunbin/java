<h1>격투게임 클래스1</h1>

```
package my1;

import java.util.*;

public class qwe1 {
	
	public static void main(String[] args) {
		qwe2 ryu = new qwe2("류", 100, 20);
		qwe2 ken = new qwe2("켄", 200, 10);

		while(true) {
			
			boolean isAlive = ryu.attack(ken);
			if(isAlive == false) {
				break;
			}
			boolean isAlive2 = ken.attack(ryu);
			if(isAlive2 == false) {
				break;
			}
		}
	}

}
```

<h2>격투게임 클래스2</h2>

```
package my1;

import java.util.Random;

public class qwe2 {
	Random r = new Random();
	String name;
	int hp;
	int max;
	
	public qwe2(String n, int h, int m) {
		name = n;
		hp = h;
		max = m;
	}
	
	public boolean attack(qwe2 enemy) {
		int d = r.nextInt(max)+1;
		enemy.hp = enemy.hp - d;
		System.out.println(name + "의 공격력은" + d + "입니다.");
		System.out.println(enemy.name + "이 공격을 받았습니다." + enemy.name + "의 현재 hp는" + enemy.hp + "입니다.");
		if(enemy.hp <= 0) {
			System.out.println(enemy.name + " 쓰러졌습니다. 게임을 종료합니다.");
			return false;
		}
		else return true;
}
}
```
