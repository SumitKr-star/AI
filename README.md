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
<br>

# 2. Write a PROLOG to implement conc(L1,L2,L3) where L2 is the list to be appended with L1 to get resulted list L3.
```
conc([], L, L).

conc([H|T], L2, [H|R]) :-
    conc(T, L2, R).
```
```
?- conc([1,2,3], [4,5], L3).
```
<br>

# 3. Write a PROLOG program to implement reverse(L,R) where list L is original and list R is reversed list.
```
reverse_list([], []).

reverse_list([H|T], R) :-
    reverse_list(T, RT),
    append(RT, [H], R).
```
```
?- reverse_list([1,2,3,4], R).
```
<br>

# 4. Write a PROLOG program to calculate the sum of two numbers.
```
sum(X, Y, S) :-
    S is X + Y.
```

# 5. Write a PROLOG program to implement max(X,Y,M) so that M is the maximum of two numbers X and Y.
