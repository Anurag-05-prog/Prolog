# Q.  Write a Prolog program, insert_nth(item, n, into_list, result) that generates a new list “result” after inserting nth element into the list “into_list”

## Code

insert_nth(Item, 0, List, [Item | List]).

insert_nth(Item, N, [Head | Tail], [Head | Result]) :-
    N > 0,
    N1 is N - 1,
    insert_nth(Item, N1, Tail, Result).

## Query

insert_nth(99, 2, [1, 2, 3, 4, 5], Result).
