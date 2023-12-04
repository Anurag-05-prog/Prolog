# Q. Find Max and Min in list

## Code

max_l([],M):- write(M).

max_l([H|T],M):-
    H >= M,
    M1 is H,
    max_l(T,M1).

max_l([H|T],M):-
    H < M,
    max_l(T,M).min_l([],M):- write(M).


min_l([H|T],M):-
    H < M,
    M1 is H,
    min_l(T,M1).

min_l([H|T],M):-
    H >= M,
    min_l(T,M).

## Query

1st - max_l([4,2,-2,7],-9999).

2nd - min_l([4,2,-2,7],9999).
