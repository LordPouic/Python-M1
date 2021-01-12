1 - Via une boucle afficher tous les chiffres entiers de 100 à 1

```
i = 0
while i < 100:
  print(100 - i)
  i = i + 1
```

2 - Via une boucle afficher tous les chiffres pairs de 1 à 100

```
i = 1
while i < 100:
  if i%2 == 0:
    print(i)
  i+=1
```

```
i = 2
while i < 100:
  print(i)
  i+=2
```

3 - Via une boucle écrire un programme qui calcule la somme des 100 premiers chiffres entiers

```
# 1 + 2 + 3 + 4 + 5 + 6 ...

Somme = 0

i = 1 
while i < 100:
  Somme += i
  i+=1

print(Somme)
```

4 - Ecrire un programme qui prend un nombre en entrée et calcule la factorielle de ce nombre.

```
# !5 -> 5*4*3*2*1

Fact = 1
i = 1
while i <= 5:
  Fact *= i
  i+=1

print(Fact) 
```

5 - Ecrire un programme ayant une variable dont la valeur est à deviner, le programme va demander en boucle une réponse et afficher soit trop haut ou trop bas tant que 
la valeur rentrée n'est pas la bonne.

```
secret_value = 10

user_value = int(input())

while secret_value != user_value:
  if user_value > secret_value:
    print("trop haut")
  else:
    print("trop bas")
  user_value = int(input())
  
print("Fin, vous avez gagné")
```

6 - Ecrire un programme qui calcule la 20eme valeur de la suite de Fibonacci.

```
# 0, 1, 1, 2, 3, 5, 8 ...
# p  c  n
#    p  c  n
previous_value = 0
current_value = 1
i=2
while i < 20:

  next_value = previous_value + current_value
  previous_value = current_value
  current_value = next_value
  i+=1

print(current_value)
```

```
FibPrevious,FibCurrent = 0, 1
i = 2
while i < 20:
  FibCurrent, FibPrevious = FibCurrent + FibPrevious, FibCurrent
  i += 1
print(FibCurrent)
```

7 - Ecrire un programme détectant les nombres de Armstrong compris entre 0 et 999.

```

```

8 - Ecrire un algorithme prenant un nombre entier donné par l'utilisateur et qui l'affiche à l'envers (12345 devient 54321)

```

```

9 - Trouver un moyen d'écrire un programme prenant un chiffre et affichant une figure comme celle ci (pour un chiffre entré de 9) :<br>
0000000000<br>
111111111<br>
22222222<br>
3333333<br>
444444<br>
55555<br>
6666<br>
777<br>
88<br>
9<br>

```

```

