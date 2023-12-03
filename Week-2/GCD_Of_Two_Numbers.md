# Q. Write a PROLOG program to find GCD of two numbers

## Code

gcd(A,0,A).

gcd(0,B,B).

gcd(A,B,G):-
    A >= B,
    M is A mod B,
    gcd(B,M,G).

gcd(A,B,G):-
    B > A,
    gcd(B,A,G).

## Query

gcd(12,18,G).
