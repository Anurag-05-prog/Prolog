# Q. Write a PROLOG program to find maximum difference among three given numbers

## Code

max(X,Y,Z,X):- X >= Y, X >= Z.

max(X,Y,Z,Y):- Y > X, Y >= Z.

max(X,Y,Z,Z):- Z > X, Z > Y.

maxdiff(A,B,C,R):-
    X is abs(A-B),
    Y is abs(B-C),
    Z is abs(A-C),
    max(X,Y,Z,R1),
    R is R1.

## Query

maxdiff(-1,2,4,R).
