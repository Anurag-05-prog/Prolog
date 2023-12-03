# Q. Write a PROLOG program to check whether a given number is odd or even

## Code

checkParity(N):-
    R is N mod 2,
    R =:= 0,
    write(N), write(' is Even.').

checkParity(N):-
    R is N mod 2,
    R =:= 1,
    write(N), write(' is Odd.').

## Query

1st - checkParity(5).

2nd - checkParity(58).
