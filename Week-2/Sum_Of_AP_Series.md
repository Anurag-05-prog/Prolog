# Q. Write a PROLOG program to find sum of A.P series ranging from X to Y with common difference D without using any formula

## Code

apSum(X,Y,_,Sum):-
    X > Y,
    write(Sum).

apSum(X,Y,D,Sum):-
    X =< Y,
    Sum1 is Sum + X,
    X1 is X + D,
    apSum(X1,Y,D,Sum1).

## Query

apSum(3,20,3,0).
