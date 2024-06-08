![](Pasted%20image%2020240606100825.png)
```mermaid
---
title: Q2 DFA
---
stateDiagram-v2
	[*] --> (1,3)
	(1,3) --> (1,3) : a
	(1,3) --> (2,4*) : b
	(2,4*) --> (2,4*) : a,b
```

## Q6 Liveness
![](Pasted%20image%2020240606110610.png)

|     | suc | gen | kill |     | in  | out | in  | out |
| --- | --- | --- | ---- | --- | --- | --- | --- | --- |
| 1   | 2   | Ø   | x    |     | Ø   | x   | Ø   | x   |
| 2   | 3   | x   | y    |     | x   | x,y | x   | x,y |
| 3   | 4,5 | x,y | Ø    |     | x,y | x   | x,y | x   |
| 4   | 5   | Ø   | z    |     | x   | x   | x   | x   |
| 5   | Ø   | x   | z    |     | x   | Ø   | x   | Ø   |

