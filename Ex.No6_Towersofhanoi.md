# Ex.No: 6   Logic Programming – Towers of Hanoi
### DATE:    26/8/2023                                                                       
### REGISTER NUMBER :212221220028 
### AIM: 
To  write  a logic program  to solve Towers of Hanoi problem  using SWI-PROLOG. 
### Algorithm:
1. Start the program
2.  Write a rules for finding solution of Towers of Hanoi in SWI-PROLOG.
3.  a )	If only one disk  => Move disk from X to Y.
4.  b)	If Number of disk greater than 0 then
5.        i)	Move  N-1 disks from X to Z.
6.        ii)	Move  Nth disk from X to Y
7.        iii)	Move  N-1 disks from Y to X.
8. Run the program  to find answer of  query.

### Program:
```
and(0,0,0).
	and(0,1,0).
	and(1,1,1).
	and(1,0,0).
	xor(0,0,0).
	xor(0,1,1).
	xor(1,0,1).
	xor(1,1,0).
	not(0,1).
	not(1,0).
	halfadder(A,B,S,C):-
	xor(A,B,S),
	and(A,B,C).
	halfsubtractor(A,B,Diff,Bo):-
	xor(A,B,Diff),
	not(A,X),
	and(B,X,Bo).

```


### Output:
![image](https://github.com/kiruthika512/AI_Lab_2023-24/assets/135616605/2fa15481-ed32-40c7-9449-16d5d3f37328)




### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.
