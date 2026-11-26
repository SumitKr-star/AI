# AI
# 1. Write a PROLOG program to implement the family tree and demonstrate the family relationship.
```
male(ram).
male(shyam).
male(mohan).

female(sita).
female(gita).

parent(ram, shyam).
parent(sita, shyam).

parent(shyam, mohan).
parent(gita, mohan).

father(X, Y) :-
    male(X),
    parent(X, Y).

mother(X, Y) :-
    female(X),
    parent(X, Y).

grandparent(X, Y) :-
    parent(X, Z),
    parent(Z, Y).
```
# 2. Write a PROLOG to implement conc(L1,L2,L3) where L2 is the list to be appended with L1 to get resulted list L3.
# 3. Write a PROLOG program to implement reverse(L,R) where list L is original and list R is reversed list.
# 4. Write a PROLOG program to calculate the sum of two numbers.
# 5. Write a PROLOG program to implement max(X,Y,M) so that M is the maximum of two numbers X and Y.
