# Q. Write a PROLOG program to print "PROLOG in Artificial Intelligence" N times

## Code

printLine(N):-
    N > 0,
    write('PROLOG in Artificial Intelligence'), nl,
    N1 is N - 1,
    printLine(N1).

## Query

printLine(5).
