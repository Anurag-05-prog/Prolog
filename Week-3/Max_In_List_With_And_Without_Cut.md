# Q. Write a Prolog program to implement maxlist(List, Max) so that Max returns the largest number in the list of numbers List (using CUT and without using CUT)

## Code

### Without Cut

maxlist([],Max):- write(Max).

maxlist([H|T],Max):-
    H >= Max,
    Max1 is H,
    maxlist(T,Max1).

maxlist([H|T],Max):-
    H < Max,
    maxlist(T,Max).

### With Cut

maxlist_cut([X], X) :- !.

maxlist_cut([H | T], Max) :-
    maxlist_cut(T, MaxTail),
    (H > MaxTail -> Max = H ; Max = MaxTail).

## Query

Without Cut - maxlist([3, 7, 2, 8, 5], -9999).

With Cut - maxlist_cut([3, 7, 2, 8, 5], Max).
