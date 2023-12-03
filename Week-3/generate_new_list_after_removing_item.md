# Q. Write a Prolog program, remove(Before, After, Item) that generates a new list “After” after the removal of “Item” from the list “Before” at all locations

## Code

remove([], [], _).

remove([Item | Tail], After, Item) :-
    remove(Tail, After, Item).

remove([Head | Tail], [Head | After], Item) :-
    Head \= Item,
    remove(Tail, After, Item).

## Query

remove([1, 2, 3, 2, 4, 2, 5], After, 2).
