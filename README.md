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

# 4. Write a PROLOG program to calculate the sum of two number.
```
sum(X, Y, S) :-
    S is X + Y.
```
<br>

# 5. Write a PROLOG program to implement max(X,Y,M) so that M is the maximum of two numbers X and Y.
```

```
# 6. Write a PROLOG program to implement factorial (N,F) where F represents the factorial of a number N.
# 7. Write a PROLOG program to implement generate_fib(N.T) where T represents the Nth term of the Fibonacci series.
# 8. Write a PROLOG program to implement power(Num, Pow, Ans) : where Num is raised to the power Pow to get Ans.
# 9. Write a PROLOG program to implement multi(N1, N2, R) : where N1 and N2 denotes the numbers to be multiplied and R represents the result.
# 10. Write a PROLOG program to implement member (X,L) : to check whether X is a member of L or not.
# 11. Write a PROLOG program to implement sumlist(L,S) so that S is the sum of a given list L.
# 12. Write a PROLOG program to implement two predicates evenlength(List) and oddlength(List) so that they are true if their argument is a list of even or odd length respectively.
# 13. Write a PROLOG program to implement maxlist(L,M) so that M is the maximum number in the list.
# 14. Write a PROLOG program to implement insert(I, N, L, R) that inserts an item I into Nth Position of list L to generate a list R.
# 15. Write a PROLOG program to implement delete(N, L, R) that removes the elements on Nth Position from a list L to generate a list R.
