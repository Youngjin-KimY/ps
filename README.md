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

<pre>'''
from collections import deque
q = deque([])
then, activate q.leftpop()
'''<code>
