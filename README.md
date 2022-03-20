# Shopee-Code-League-2022
https://www.hackerearth.com/challenges/competitive/shopee-code-league-2022-qualification-round/?login=e3fd022c91862790b3b70b1f7078a301
Money Transfer
Max. score: 100

SeaMoney has a feature to transfer money between users. Let’s imagine a simple scenario.

 usernames—consisting of lowercase Latin characters—each starts with a balance . Amongst them,  transactions happened, where user transfers  amount of money to . If is larger than the

’s balance when the transaction happens, the transaction is automatically rejected.

Output the final balance of each user.

Input

The first line contains two numbers
 and . Each of the next  following lines contain username   and integer , denoting the balance of user . Following that are  lines, each containing two usernames  and   followed by an integer , denoting the amount of money transferred from  to 

 .

Output

Output the balance of all users in alphabetical order.
SAMPLE INPUT

3 4
amir 10
brenda 10
charlie 10
amir brenda 5
brenda charlie 5
charlie amir 20
charlie amir 7

SAMPLE OUTPUT

amir 12
brenda 10
charlie 8

/* IMPORTANT: Multiple classes and nested static classes are supported */

/*
 * uncomment this if you want to read input.
//imports for BufferedReader
import java.io.BufferedReader;
import java.io.InputStreamReader;

//import for Scanner and other utility classes
import java.util.*;
*/

// Warning: Printing unwanted or ill-formatted data to output will cause the test cases to fail

class TestClass {
    public static void main(String args[] ) throws Exception {
        /* Sample code to perform I/O:
         * Use either of these methods for input

        //BufferedReader
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String name = br.readLine();                // Reading input from STDIN
        System.out.println("Hi, " + name + ".");    // Writing output to STDOUT

        //Scanner
        Scanner s = new Scanner(System.in);
        String name = s.nextLine();                 // Reading input from STDIN
        System.out.println("Hi, " + name + ".");    // Writing output to STDOUT

       */

        // Write your code here

    }
}

    private int findMinStep(int[][] grid) {
//        for (int i = 0; i < grid.length; i++) {
//            for (int j = 0; j < grid[0].length; j++) {
//
//                if(grid[i][j] != 0){
//                    dfs(grid, i, j);
//
//                }
//            }
//        }
        if(grid == null || grid.length == 0)
            return 0;
        int row = grid.length;
        int col = grid[0].length;

        int[][] cache = new int[row][col];
        cache[0][0] = grid[0][0];
        for(int i = 1; i < col; i++) {
            cache[0][i] = cache[0][i-1] + grid[0][i];
        }
        for(int j = 1; j < row; j++) {
            cache[j][0] = cache[j-1][0] + grid[j][0];
        }
        for(int i=1; i<row; i++) {
            for(int j=1; j<col; j++) {
                System.out.println("cache[" + (i-1) + "][" + j + "] = " + cache[i-1][j] + " cache[" + i + "][" + (j-1) + "]=" + cache[i][j-1]);
                if(cache[i-1][j] > cache[i][j-1]) {
                    cache[i][j] = cache[i][j-1] + grid[i][j];
                    System.out.println("[" + i + "," + (j-1) + "] =" + grid[i][j-1]);
                } else {
                    cache[i][j] = cache[i-1][j] + grid[i][j];
                    System.out.println("[" + (i-1) + "," + j + "] =" + grid[i-1][j]);
                }
                System.out.println("cache[" + i + "][" + j + "] = " + cache[i][j]);
            }
        }
        System.out.println("[" + (row -1) + "," + (col - 1) + "] =" + grid[row-1][col-1]);
        return cache[row-1][col-1];
    }

============================================================================================================================================
Installation of a Shopee Billboard
Max. score: 100

You are installing a billboard and want it to be at the maximum height. The billboard will have two steel supports, one on each side. The height of each steel bracket must be equal.

You have a number of rebar rods that can be welded together. For example, if the bars are of length 1, 2, and 3, they can be welded together to form a length of 6 brackets.

Return the maximum possible installation height of the billboard. Return 0 if the billboard cannot be installed.
SAMPLE INPUT

4
1 2 3 6

SAMPLE OUTPUT

6

Explanation

input: [1, 2, 3, 6]

output： 6
==================================================================================================================================================================================================================================================
Bob is a Shopee Xpress deliveryman and is delivering a package to his destination. He started his journey from one of our Shopee warehouses at position (0, 0), and his destination is at the bottom-right corner of the map. For example, if the map is an 8x8 grid, the destination is (7, 7).

Each step, his car can move 1 square up, down, left, or right. If his car reaches a black hole, it can teleport to any other location connected to the black hole at no cost, he also can skip the teleport feature. For example, if the car reaches black hole A at position (1, 1), Bob can teleport to position (0, 5) without costing an additional step.

Find the least number of steps (shortest path) that Bob can take to move from (0, 0) to the destination.

So, one path of least steps for example map is:

0,0 -> 0,1 -> 1,1/0,5 -> 1,5-> 1,6/7,3 -> 7,2 -> 6,2/6,7-> 7.7 , the answer is 7.

Input: 

The first line contains two numbers M, N (

). M refers to the number of rows in the map, and N refers to the number of columns in the map.

The next M rows contain N values xij ( 

 ), where 0 means that position ( i, j ) is an empty square, and non-zero values mean that a black hole is present in the square. Non-zero values are guaranteed to have at least 2 or more instances on the map.

Output: 

To print the integer of the least number of steps needed.


/* IMPORTANT: Multiple classes and nested static classes are supported */

/*
 * uncomment this if you want to read input.
//imports for BufferedReader
import java.io.BufferedReader;
import java.io.InputStreamReader;
x`
//import for Scanner and other utility classes
import java.util.*;
*/

// Warning: Printing unwanted or ill-formatted data to output will cause the test cases to fail

class TestClass {
    public static void main(String args[] ) throws Exception {
        /* Sample code to perform I/O:
         * Use either of these methods for input

        //BufferedReader
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String name = br.readLine();                // Reading input from STDIN
        System.out.println("Hi, " + name + ".");    // Writing output to STDOUT

        //Scanner
        Scanner s = new Scanner(System.in);
        String name = s.nextLine();                 // Reading input from STDIN
        System.out.println("Hi, " + name + ".");    // Writing output to STDOUT

        */

        // Write your code here

    }
}




===========================================================================================================================================
@SuppressWarnings("boxing")
	private static void balance(String line) {
		Map<String, Integer> balanceMap = new HashMap<>();
		List<Transaction> transactions = new ArrayList<>();
		for(Transaction transaction: transactions) {
			if(transaction.getTransactionAmount() < balanceMap.get(transaction.getDeliverer())) {
				String deliverer = transaction.getDeliverer();
				String receiver = transaction.getReceiver();
				balanceMap.put(deliverer, Integer.valueOf(balanceMap.get(deliverer) - transaction.getTransactionAmount()));
				balanceMap.put(receiver, Integer.valueOf(balanceMap.get(receiver) + transaction.getTransactionAmount()));
			}
		}
		
		for(String user: balanceMap.keySet()) {
			System.out.print(user+" "+balanceMap.get(user));
		}
	}

	public class Transaction {
		String receiver; // receiver
		String deliverer; // first person in line (deliverer)
		Integer transactionAmount;

		public String getReceiver() {
			return receiver;
		}

		public void setReceiver(String receiver) {
			this.receiver = receiver;
		}

		public String getDeliverer() {
			return deliverer;
		}

		public void setDeliverer(String deliverer) {
			this.deliverer = deliverer;
		}

		public Integer getTransactionAmount() {
			return transactionAmount;
		}

		public void setTransactionAmount(Integer transactionAmount) {
			this.transactionAmount = transactionAmount;
		}
    
  ====================================================================================================================================================================================
  static int billboard(int a, int ...b) {
		int arr[] = Arrays.stream(b).toArray();
		Arrays.sort(arr);
		int i; int n = arr.length -1;
		int max = 0; int max_left = arr[0];
		int max_right = arr[n];
		for(i = 1; i<n;i++) {
			if(max_left<max_right) {
				max_left += arr[i];

			}
			if(max_right< max_left) {
				max_right += arr[n-1];
			}
			if(max_left == max_right) {
				max = max_left;
			}
		}
		
		return max;
	}

	}
