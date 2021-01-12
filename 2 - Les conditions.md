1 - Faire un programme qui prend l'age d'une personne et qui affiche si cette personne est majeure ou non.

```
Age = int(input())
if Age >= 18:
  print("Majeur")
else:
  print("Mineur")
```

2 - Faire un programme qui prend deux valeurs et qui affiche la plus petite des deux

```
A = 2
B = 4
if A < B:
  print(A)
else:
  print(B)
```

3 - Même exercice que le 2 mais cette fois le programme prend 3 valeurs

```
A = -5
B = 1
C = 6

if A < B and A < C: 
  print(A)
elif B < C:
  print(B)
else:
  print(C)
```

4 - Ecrire un programme qui détecte si une année est bissextile

```
year = 8
if (year%4 == 0 and year%100 != 0) or year%400 == 0:
  print("Bisex")
```

