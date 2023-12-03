# Q. Write a Prolog program to append for two lists

## Code

append([],L2,L2).

append([H|T],L2,[H|L3]):-
    append(T,L2,L3).

## Query

append([1,2,3],[4,5,6,7],L3).
