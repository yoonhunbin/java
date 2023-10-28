<h1>w자동차</h1>
```
package homework;

import java.util.Random;

public class Car {
	String carName;
	int speed; //차동차 이름
	int max; //자동차 현재 최고 속도
	int acc; //최고 가속도
	int km; //주행거리
	Random r = new Random();
	
	public Car(String c, int m, int a) {
		carName = c;
		max = m;
		acc = a;
	}
	
	public void speedUp() {
		int a = r.nextInt(acc) + 1;
		speed += a;
		if(speed > max) speed = max;
		km += speed;
		System.out.println(carName + "의 현재속도는" + speed + "입니다");
		a += 1;
	}
	public void speedDown() {
		int b = r.nextInt(acc) + 1;
		speed -= b;
		if(speed < 0) {
		speed = 0;
		}
		km += speed;
		System.out.println(carName + "의 현재속도는" + speed + "입니다");
		}
	public void stop() {
		System.out.println(carName + "의 현재속도는" + speed + "입니다");
	}
	
	public void printkm() {
		System.out.println(carName + "의 현재까지 주행거리는" + km + "입니다");
	}
	}
 ```
