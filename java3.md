전사와 마법사 전투
```java
package homework;

import java.util.Random;
import java.util.Scanner;

public class Myprofile5 {
	public static void main(String[] args) {
		int wizardH = 10;
		int warriorH = 20;

		Random random = new Random();

		Scanner scanner = new Scanner(System.in);

		System.out.print("공격하려면 1을 누르세요. 외 숫자를 입력하면 종료합니다.");
		int choice = scanner.nextInt();

		if (choice == 1) {
			int wizardD = random.nextInt(11) + 15;
			int warriorD = random.nextInt(11) + 5;

			warriorH = warriorH - wizardD;
			wizardH = wizardH - warriorD;

			System.out.println("마법사 HP: " + wizardH + ", 전사 HP: " + warriorH);
			if (warriorH <= 0 && wizardH <= 0)
				System.out.println("마법사와 전사가 동시에 죽었습니다.");

			else if (warriorH <= 0)
				System.out.println("마법사가 이겼습니다. 전사가 죽었습니다.");

			else if (wizardH <= 0)
				System.out.println("전사가 이겼습니다. 마법사가 죽었습니다.");

			else
				System.out.println("종료합니다.");

			scanner.close();
		}
	}
}
```

