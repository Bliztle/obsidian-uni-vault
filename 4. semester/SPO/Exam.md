Q1 should only have 1 parenthesis at the end
![](Pasted%20image%2020240611100540.png)
```mermaid
---
title: Q2 DFA
---
stateDiagram-v2
	[*] --> (1,2)
	(1,2) --> (2,3,4) : a
	(1,2) --> (2) : b
	(2,3,4) --> (2,3) : a
	(2,3,4) --> (2,5) : b
	(2) --> (2,3) : a
	(2) --> (2) : b
	(2,3) --> (2,3) : a
	(2,3) --> (2) : b
	(2,5) --> (2,3) : a
	(2,5) --> (2) : b
```
Solution doesn't have {2} in aab, only 2

![](Pasted%20image%2020240611101921.png)

|     | N?    | N?    | N?    |
| --- | ----- | ----- | ----- |
| A   | false | false | false |
| B   | false | true  | true  |
| C   | false | false | false |

$First(A)=\{x\}$
$First(B)=\{z\}$
$First(C)=\{y,z,x\}$

$Follow(A)=\{\}$
$Follow(B)=\{x,y\}$
$Follow(C)=\{z\}$

$Follow(A)=\{\}$
$Follow(B)=\{x,y\}$
$Follow(C)=\{z,y\}$

![](Pasted%20image%2020240611114823.png)
There is a non-sensical sentence (option 3). Hopefully it is not the answer meant to be correct.

![](Pasted%20image%2020240611104524.png)

| Line | Succ | Gen | Kill |     | In  | Out | In  | Out |
| ---- | ---- | --- | ---- | --- | --- | --- | --- | --- |
| 1    | 2    | Ø   | x    |     | Ø   | x   | Ø   | x   |
| 2    | 3    | Ø   | y    |     | x   | x,y | x   | x,y |
| 3    | 4    | x,y | x    |     | x,y | x,y | x,y | x,y |
| 4    | 3,5  | y   | Ø    |     | x,y | x,y | x,y | x,y |
| 5    | 6    | x   | z    |     | x,y | y,z | x,y | y,z |
| 6    | Ø    | y,z | y    |     | y,z | Ø   | y,z | Ø   |

![](Pasted%20image%2020240611105634.png)
