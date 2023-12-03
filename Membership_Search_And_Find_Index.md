# Q. Check if an element is present in the list or not. If present then return the index

## Code

isPresent([],_,_):- write('Not Present').

isPresent([H|_],E,I):-
    H =:= E,
    I1 is I + 1,
    write('Present'),
    nl,
    write('Found at '), write(I1).

isPresent([H|T],E,I):-
    H \= E,
    I1 is I + 1,
    isPresent(T,E,I1).

## Query

1st - isPresent([5,2,6],9).

2nd - isPresent([5,2,6],5).
