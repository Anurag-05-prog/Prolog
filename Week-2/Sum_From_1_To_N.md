# Q. Write a PROLOG program to find sum of numbers ranging from 1 to N without using any formula

## Code

sumRange(I,N,S):-
    I > N,
    write(S).

sumRange(I,N,S):-
    I =< N,
    S1 is S + I,
    I1 is I + 1,
    sumRange(I1,N,S1).

## Query

sumRange(1,5,0).
