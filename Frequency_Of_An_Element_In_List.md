# Q. Find the frequency of an element given as input in a list

## Code

freq_l([],_,F):- write(F).

freq_l([H|T],E,F):-
    H =:= E,
    F1 is F + 1,
    freq_l(T,E,F1).

freq_l([H|T],E,F):-
    H \ = E,
    freq_l(T,E,F).

## Query

freq_l([2,1,2,4,8,2,3],2,0).
