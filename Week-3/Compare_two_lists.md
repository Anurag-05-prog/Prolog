# Q.  Write a Prolog program that compares two lists and returns the number of locations where they differ (element wise)

## Code

compare_lists([], [], 0).

compare_lists([X | Xs], [Y | Ys], Count) :-
    X \= Y,
    compare_lists(Xs, Ys, RestCount),
    Count is RestCount + 1.

compare_lists([X | Xs], [X | Ys], Count) :-
    compare_lists(Xs, Ys, Count).

## Query

compare_lists([1, 2, 3, 4], [1, 2, 5, 4], Count).
