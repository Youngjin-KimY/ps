# Problem Solving
## Purpose of this document is describing new algorithm I study and checking my fault, when I meet new problem

### 2019.02.28
1. gcd and lcm
<pre><code>
class Solution:
    def __init__(self):
        self.__t = int(input())
        self.__sol()

    def __sol(self):
        for i in range(0,self.__t):
            a,b = map(int,input().split())
            print(self.__lcm(a,b))

    def __gcd(self,a,b):
        if a>b:
            tmp = a
            a = b
            b = tmp
	
	# a < b
        while a != 0:
            n = b%a
            b = a
            a = n

        return b

    def __lcm(self,a,b):

        return int(a*b/self.__gcd(a,b))
	
if __name__ == "__main__":
    s = Solution()
</pre></code>

Above code is that gcd and lcm, using euclidean method to solve this sort of problems.


### 2019.01.06 
1. matching paranthesis problem
	* edge cases 
		1) matched, but remain paranthesis
		2) size of string is 0 -> true
		3) size of string is 1 -> false
		

### 2019.01.08
1. LeetCode 654 Maximum Binary Tree Problem
	intuition
	- find index of maximum value
	- divide list as two part, criterion is maximum value
	

### 2019.01.24 
boj_2252: topological ordering, i don't understand why is this prob in the PQ..
first, checking in-degree of every vertices.
second, there are some of 0 in-degree vertices, push into stack. and simultaneously the vertices decreses in-degree from vertices which is going to push into the stack.
repeatly some vertices decreases in degree, and if in-degree is 0, than go to stack. until q is 0

- how to use queue in the python

<pre><code>
	from collections import deque
	q = deque([])
	then, activate q.leftpop()
</pre></code>
### 2019.01.31
1. boj11726
DP : deployment of card



### 2019.01.30
1. I didn't care about using "in" with list, I mean that I wanted to check whether some variable is in the list or not,
and I uses like this statement.

<pre><code>
	if seeV in somelist: 
		doing
	-> actually this is like using for statement, it takes o(n)
</pre></code>

2. about using sys.stdin.readline()
sys.stdin.readline() operation takes "\n" line breaks, so we have to check end of input has "\n" of line break. 
we can easily change "\n" with operation replace which is in the string
<pre><code>
e.g sys.stdin.readline().replace("\n","")
</pre></code>
at that thme, if original string is like "Kim\n", then the string will be changed as "Kim"

3. set data structure
today's concept of problem takes finding intersaction between two sets.
at this time, we have two choices, 1) sets 2) dict which is hash in other programming languages
set has intersact operataton and dict can acess data o(1) with elements
<pre><code>
setA=(1,2,3)
setB=(3,4,5)
setA.intersaction(setB)
>> {3}
</pre></code>

### 2019.01.31
1. floyd warshall algorithm : boj11404<br>
time complexity : O(n<sup>3</sup>)<br>
space complexity : O(n<sup>2</sup>)<br>

funny thing is that algorithm is implemented by 3 inner for loop, and most outer loop shows mid point road.

by python3 
<pre><code>
for k in range(1,v+1):
   for i in range(1,v+1):
      for j in range(1,v+1):
         if adj[i][j] > adj[i][k]+adj[k][k]:
	    adj[i][j] = adj[i][k]+adj[k][k]

</pre></code>



