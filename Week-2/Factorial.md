# Q. Write a PROLOG program to determine the factorial of a given number

## Code

fact(0,1).

fact(1,F):-
    write(F).

fact(N,F):-
    N > 1,
    F1 is F*N,
    N1 is N - 1,
    fact(N1,F1).

## Query

fact(5,1).
