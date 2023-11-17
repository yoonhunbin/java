<h1>자동차.class</h1>


```
package homework;

import java.util.Scanner;

public class Car2 {
	
	public static void main(String[] args) {
		Scanner s = new Scanner(System.in);
		Car car1 = new Car("윤현빈", 200, 100);
		int a = 0;
		
		System.out.println("자동차 게임을 시작합니다.");
		
	while(car1.km < 5000) {
		System.out.println("엑셀(1), 감속(2), 정지(3), 주행거리표시(4)");
		int input = s.nextInt();
		
		if(input == 1) {
			car1.speedUp();
			a += 1;
		}
		else if(input == 2) {
			car1.speedDown();
			a += 1;
		}
		else if(input == 3) {
			car1.stop();
			a += 1;
		}
		else if(input == 4)car1.printkm();
		System.out.println("횟수:" + a);
	}
  }
}
```
