# Q. Length of the list

## Code

len([],L):-write(L).

len([_|T],L):-
    L1 is L + 1,
    len(T,L1).

## Query

len([5,2,9,5],L).
