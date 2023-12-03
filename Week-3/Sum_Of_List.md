# Q. Write a Prolog program to implement sumlist(List,Sum) so that Sum returns the sum of a given list of numbers List

## Code

sumlist([],Sum):- write(Sum).

sumlist([H|T],Sum):-
    Sum1 is Sum + H,
    sumlist(T,Sum1).

## Query

sumlist([3, 7, 2, 8, 5], 0).
