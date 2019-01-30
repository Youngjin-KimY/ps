# Problem Solving
## Purpose of this document is describing new algorithm I study and checking my fault, when I meet new problem

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

<pre>
	from collections import deque
	q = deque([])
	then, activate q.leftpop()
<code>

### 2019.01.30
1. I didn't care about using "in" with list, I mean that I wanted to check whether some variable is in the list or not,
and I uses like this statement.

<pre>
	if seeV in somelist: 
		doing
	-> actually this is like using for statement, it takes o(n)
<code>

2. about using sys.stdin.readline()
sys.stdin.readline() operation takes "\n" line breaks, so we have to check end of input has "\n" of line break. 
we can easily change "\n" with operation replace which is in the string
<pre>
e.g sys.stdin.readline().replace("\n","")
<code>
at that thme, if original string is like "Kim\n", then the string will be changed as "Kim"

3. set data structure
today's concept of problem takes finding intersaction between two sets.
at this time, we have two choices, 1) sets 2) dict which is hash in other programming languages
set has intersact operataton and dict can acess data o(1) with elements
<pre>
setA=(1,2,3)
setB=(3,4,5)
setA.intersaction(setB)
>> {3}

<code>
