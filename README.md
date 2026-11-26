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
max(X, Y, X) :-
    X >= Y.

max(X, Y, Y) :-
    Y > X.
```
```
?- max(10, 20, M).
```
<br>

# 6. Write a PROLOG program to implement factorial (N,F) where F represents the factorial of a number N.
```
factorial(0, 1).

factorial(N, F) :-
    N > 0,
    N1 is N - 1,
    factorial(N1, F1),
    F is N * F1.
```
```
?- factorial(5, F).
```
<br>

# 7. Write a PROLOG program to implement generate_fib(N.T) where T represents the Nth term of the Fibonacci series.
```
generate_fib(0, 0).

generate_fib(1, 1).

generate_fib(N, T) :-
    N > 1,
    N1 is N - 1,
    N2 is N - 2,
    generate_fib(N1, T1),
    generate_fib(N2, T2),
    T is T1 + T2.
```
```
?- generate_fib(6, T).
```
<br>

# 8. Write a PROLOG program to implement power(Num, Pow, Ans) : where Num is raised to the power Pow to get Ans.
```
power(_, 0, 1).

power(Num, Pow, Ans) :-
    Pow > 0,
    P1 is Pow - 1,
    power(Num, P1, A1),
    Ans is Num * A1.
```
```
?- power(2, 3, Ans).
```
<br>

# 9. Write a PROLOG program to implement multi(N1, N2, R) : where N1 and N2 denotes the numbers to be multiplied and R represents the result.
```
multi(N1, N2, R) :-
    R is N1 * N2.
```
```
?- multi(5, 4, R).
```
<br>

# 10. Write a PROLOG program to implement member (X,L) : to check whether X is a member of L or not.
```
memb(X, [X|_]).

memb(X, [_|T]) :-
    memb(X, T).
```
```
?- memb(3, [1,2,3,4]).
```
<br>

# 11. Write a PROLOG program to implement sumlist(L,S) so that S is the sum of a given list L.
```
sumlist([], 0).

sumlist([H|T], S) :-
    sumlist(T, S1),
    S is H + S1.
```
```
?- sumlist([1,2,3,4], S).
```
# 12. Write a PROLOG program to implement two predicates evenlength(List) and oddlength(List) so that they are true if their argument is a list of even or odd length respectively.
```
evenlength([]).

evenlength([_,_|T]) :-
    evenlength(T).

oddlength([_]).

oddlength([_,_|T]) :-
    oddlength(T).
```
```
?- evenlength([1,2,3,4]).
```
# 13. Write a PROLOG program to implement maxlist(L,M) so that M is the maximum number in the list.
# 14. Write a PROLOG program to implement insert(I, N, L, R) that inserts an item I into Nth Position of list L to generate a list R.
# 15. Write a PROLOG program to implement delete(N, L, R) that removes the elements on Nth Position from a list L to generate a list R.
