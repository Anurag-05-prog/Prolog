# Q. Write a PROLOG program to find sum of G.P series ranging from X to Y with common divisor D without using any formula

## Code

gpSum(X,Y,_,P):-
    X > Y,
    write(P).

gpSum(X,Y,C,P):-
    X =< Y,
    P1 is P*X,
    X1 is X*C,
    gpSum(X1,Y,C,P1).

## Query

gpSum(3,20,3,1).
