1~100까지의 합
```java
package homework;

public class Myprofile {
	public static void main(String[] args) {
		int num1 = 0;
		int i = 1;
		
		while(i<=100) {
			num1 = num1 + i;
			i++;
		}
System.out.print("1~100까지의 합" + num1);		
		
    }	
	}
```

100개의 숫자중 중복없이 3개 뽑기
```java
package homework;

import java.util.*;

public class Myprofile2 {
	public static void main(String[] args) {
		Random r1 = new Random();
		
		int one = r1.nextInt(100)+1;
		
		int two = r1.nextInt(100)+1;
		while(two == one) {
			two = r1.nextInt(100)+1;
		}
		
		int three = r1.nextInt(100)+1;
		while((one==three)&(three==two)) {
			three = r1.nextInt(100)+1;
		}
		
		System.out.println("뽑힌 숫자는" + one + "," + two + "," + three);
    }
	}
```

```java
import java.utli.*;

Random r = new Random();  
Scanner s = new Scanner(System.in);  
```
`Random` = 난수 만들기  
`Scanner` = 파이썬의 input하고 비슷하다.
