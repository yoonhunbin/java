<h1>보스 게임 (Game)</h1>

```
package asd1;

import java.util.Random;

public class Game {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Random r = new Random();
		ch player = new ch("윤현빈", 200, 15);
		boss boss = new boss("보스", 300, 20);
		
		while(true) {
			int f = r.nextInt(5) + 1;
			boolean num1 = player.attack(boss);
			if(num1 == false) {
				break;
			}
			if(f == 5) {
				boolean num2 = boss.sattack(player);
				if(num2 == false) {
					break;
				}
			}
			else if(f != 5) {
				boolean num2 = boss.battack(player);
				if(num2 == false) {
					break;
				}
			}
		}

	}

}
```

<h2> 보스 게임 (Boss)</h2>

```
package asd1;

public class boss extends ch{
	public boss(String name, int hp, int max) {
		super(name, hp, max);
	}
	
	public boolean battack(ch n) {
		int d = r.nextInt(max) + 1;
		int a = n.getHp() - d;
		n.setHp(a);
		System.out.println(name + "의 공격력은" + d + "입니다.");
		System.out.println(n.name + "이 공격을 받았습니다." + n.name + "의 현재 hp는" + a + "입니다.");
		if (n.getHp() <= 0) {
			System.out.println(n.name + " 쓰러졌습니다. 게임을 종료합니다.");
			return false;
		} else
			return true;
	}
	
	public boolean sattack(ch n) {
		int a = n.getHp() - max;
		n.setHp(a);
		int b = getHp() - 10;
		n.setHp(b);
		System.out.println("보스 필살기 발동" + n.name + "의 체력" + a + " " + name + "의 체력" + b + "입니다");
		if(n.getHp() <= 0) {
			System.out.println(n.name + "쓰러졌습니다. 게임을 종료합니다.");
			return false;
		}
		else return true;
	}

}
```

<h2>보스 게임 (Ch)</h2>

```
package asd1;

import java.util.Random;

public class ch {
	Random r = new Random();
	String name;
	private int hp;
	int max;

	ch(String name, int hp, int max) {
		this.name = name;
		this.hp = hp;
		this.max = max;
	}

	public int getHp() {
		return hp;
	}

	public void setHp(int hp) {
		this.hp = hp;
	}

	public boolean attack(boss n) {
		int d = r.nextInt(max) + 1;
		int b = n.getHp() - d;
		n.setHp(b);
		System.out.println(name + "의 공격력은" + d + "입니다.");
		System.out.println(n.name + "이 공격을 받았습니다." + n.name + "의 현재 hp는" + b + "입니다.");
		if (n.getHp() <= 0) {
			System.out.println(n.name + " 쓰러졌습니다. 게임을 종료합니다.");
			return false;
		} else
			return true;
	}
}
```
