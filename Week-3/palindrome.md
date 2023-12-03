# Q. Write a Prolog program to implement palindrome(List)

## Code

isPalindrome([]).

isPalindrome([_]).

isPalindrome(L):-
    append([First|Middle],[Last],L),
    First =:= Last,
    isPalindrome(Middle).

## Query

1st - isPalindrome([2,3,1,3,2]).

2nd - isPalindrome([2,4,3,1]).
