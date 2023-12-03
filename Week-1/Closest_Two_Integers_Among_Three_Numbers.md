# Q. Write a PROLOG program to find closest two integers among three given integers

## Code

min(X,Y,Z,X):- X =< Y, X =< Z.

min(X,Y,Z,Y):- Y < X, Y =< Z.

min(X,Y,Z,Z):- Z < X, Z < Y.

closest(A,B,C,R):-
    X is abs(A-B),
    Y is abs(B-C),
    Z is abs(A-C),
    min(X,Y,Z,R1),
    R is R1.

## Query

closest(-1,2,4,R).
