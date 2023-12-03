# Q.  Write a Prolog program to implement reverse(List,ReversedList) that reverses a list

## Code

reverse([],[]).

reverse([H|T],L):-
    reverse(T,L1),
    append(L1,[H],L).

## Query

reverse([2,3,1,5,7],L).
