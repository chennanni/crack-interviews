## Shell Test

Given a text file file.txt, print just the 10th line of the file.

~~~
Example:
Assume that file.txt has the following content:
Line 1
Line 2
Line 3
Line 4
Line 5
Line 6
Line 7
Line 8
Line 9
Line 10

Your script should output the tenth line, which is:
Line 10
~~~

### Awnser

~~~
# Solution 1
cnt=0
while read line && [ $cnt -le 10 ]; do
  let 'cnt = cnt + 1'
  if [ $cnt -eq 10 ]; then
    echo $line
    exit 0
  fi
done < file.txt

# Solution 2
awk 'FNR == 10 {print }' file.txt
# OR
awk 'NR == 10' file.txt

# Solution 3
sed -n 10p file.txt

# Solution 4
tail -n+10 file.txt|head -1
~~~

## SQL Test

Write a SQL query to get the second highest salary from the Employee table.

~~~
+----+--------+
| Id | Salary |
+----+--------+
| 1  | 100    |
| 2  | 200    |
| 3  | 300    |
+----+--------+
~~~
For example, given the above Employee table, the query should return 200 as the second highest salary. If there is no second highest salary, then the query should return null.

~~~
+---------------------+
| SecondHighestSalary |
+---------------------+
| 200                 |
+---------------------+
~~~

### Awswer

~~~
select Email
from Person
group by Email
having count(*)>1;
~~~

## Code Test - 2 Sum

Given an array of integers, return indices of the two numbers such that they add up to a specific target.

~~~
Given nums = [2, 7, 11, 15], target = 9,
Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
~~~

~~~
public class Solution {
	public int[] twoSum(int[] numbers, int target) {
		// TODO
	}
}
~~~

## Code Test - Binary Gap

Given a positive integer N, find and return the longest distance between two consecutive 1's in the binary representation of N.
If there aren't two consecutive 1's, return 0.

~~~
Example 1:
Input: 22
Output: 2
Explanation: 
22 in binary is 0b10110.
In the binary representation of 22, there are three ones, and two consecutive pairs of 1's.
The first consecutive pair of 1's have distance 2.
The second consecutive pair of 1's have distance 1.
The answer is the largest of these two distances, which is 2.
~~~

~~~
Example 2:
Input: 5
Output: 2
Explanation: 
5 in binary is 0b101.
~~~

~~~
Example 3:
Input: 6
Output: 0
Explanation: 
6 in binary is 0b110.
~~~

~~~
Example 4:
Input: 8
Output: 0
Explanation: 
8 in binary is 0b1000.
There aren't any consecutive pairs of 1's in the binary representation of 8, so we return 0.
~~~

~~~
public int binaryGap(int N) {
	// TODO
}
~~~

## Code Test - SimpleList

Implement a SimpleList, which is similar to ArrayList.

~~~
public class SimpleList<T> {
	private Object[] elementData;
	private int size=0;
	public int size() {
		// TODO
		return -1;
	}
	public SimpleList() {
		// TODO
	}
	public boolean isEmpty() {
		// TODO
		return false;
	}
	public boolean add(T e) {
		// TODO
		return false;
	}
	public boolean remove(Object o) {
		// TODO
		return false;
	}
	public T get(int index) {
		// TODO
		return null;
	}
}
~~~
