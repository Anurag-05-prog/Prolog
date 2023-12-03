# Q. Write a PROLOG program to find the maximum of two given numbers

## Code

max(X,Y,X):- X >= Y.

max(X,Y,Y):- Y > X.

## Query

1st - max(4,-1,R).

2nd - max(6,15,R).
