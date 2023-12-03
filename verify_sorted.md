# Q. Check if the list is sorted or not

## Code (For Ascending Order)

isSorted([],_):- write('Sorted').

isSorted([H|T],M):-
    H >= M,
    M1 is H,
    isSorted(T,M1).

isSorted([H|_],M):-
    H < M,
    write('Not Sorted').

## Code (For Descending Order)

isSorted([],_):- write('Sorted').

isSorted([H|T],M):-
    H =< M,
    M1 is H,
    isSorted(T,M1).

isSorted([H|_],M):-
    H > M,
    write('Not Sorted').

## Query

For Ascending Order - isSorted([4,4,8,9],-9999).

For Descending Order - isSorted([9,8,4,4],9999).
