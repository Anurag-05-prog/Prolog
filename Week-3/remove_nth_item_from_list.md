# Q. Write a Prolog program to remove the N-th item from a list

## Code

remove_nth(1, [_ | Tail], Tail).

remove_nth(N, [Head | Tail], [Head | Result]) :-
    N > 1,
    N1 is N - 1,
    remove_nth(N1, Tail, Result).

## Query

remove_nth(2, [1, 2, 3, 4, 5], Result).
