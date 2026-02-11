##CodeForces Practice Problems

1. [https://codeforces.com/problemset/problem/1875/A](https://codeforces.com/problemset/problem/1875/A)
	
	**Concept:** Greedy accumulation with an upper bound per addition.
		1. Initialise total time
		Start with count = b (initial timer).
		Add Capped increments
		2.For each of the n values x, add
		min(x, a - 1)
		This ensures no single addition exceeds the allowed maximum.
		 Output the final accumulated count.
```java
import java.util.Scanner;
 
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
 
        while (t-- > 0) {
            long a = sc.nextInt();
            long b = sc.nextInt();
            int n = sc.nextInt();
 
            long count = b;   // initial timer = initial seconds
 
            for (int i = 0; i < n; i++) {
                long x = sc.nextInt();
                count += Math.min(x, a - 1);
            }
 
            System.out.println(count);
        }
    }
}
```



2. https://codeforces.com/problemset/problem/1899/A
	If `n` is divisible by 3, the second player wins; otherwise, the first player wins.
	Implementation
	
```java
	import java.util.Scanner;
	public class game_with_integer {
	    public static void main(String[] args) {
	        Scanner sc=new Scanner(System.in);
	        int t=sc.nextInt();
	        while(t-->0){
	            int n=sc.nextInt();
	            System.out.println(n%3==0 ? "Second" : "First");
	        }
	    }
	}
```

3. https://codeforces.com/problemset/problem/1903/A
	If `k > 1`, any arrangement is possible because multiple operations allow rearranging the array freely.
	
	If `k == 1`, the array cannot be rearranged. Therefore, the array must already be sorted.

```java
import java.util.*;
public class HalloumiBoxes {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int t = scanner.nextInt();
        while (t-- > 0) {
            int n = scanner.nextInt();
            int k = scanner.nextInt();
            long[] a = new long[n];
            for (int i = 0; i < n; i++) {
                a[i] = scanner.nextLong();
            }
            long[] sorted = a.clone();
            Arrays.sort(sorted);
            if (k > 1) System.out.println("YES");
            else System.out.println(Arrays.equals(sorted, a) ? "YES" : "NO");
        }
    }
}
```

4. 
