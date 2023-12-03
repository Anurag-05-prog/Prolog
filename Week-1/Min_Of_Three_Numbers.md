# Q. Write a PROLOG program to find the minimum of three given numbers

## Code

min(X,Y,Z,X):- X =< Y, X =< Z.

min(X,Y,Z,Y):- Y < X, Y =< Z.

min(X,Y,Z,Z):- Z < X, Z < Y.

## Query

1st - min(4,2,-1,R).

2nd - min(8,5,3,R).

3rd - min(9, 16, 25, R).
