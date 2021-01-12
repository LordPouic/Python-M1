
1 - Ecrire un programme ayant une variable C, donner une valeur à C, calculer et afficher son carré

```
c = int(input())

c *= c 

print(c)
```

2 - Ecrire un programme ayant deux variable A et B, donner des valeurs à A et B puis tenter de trouver quatre moyens d’intervertir les deux valeurs contenues dans A et B

```
A = 2
B = 3
print(A,B)

Tmp = A
A = B
B = Tmp
del Tmp

print(A,B)
```

```
A = 2
B = 3
print(A,B)

A = A + B
B = A - B
A = A - B

print(A,B)
```

```
A = 2
B = 3
print(A,B)

A = A ^ B
B = A ^ B
A = A ^ B 

print(A,B)
```

```
A = 2
B = 3
print(A,B)

A,B = B,A

print(A,B)
```

3 - Ecrire un programme ayant une variable R correspondant au rayon d’un cercle, donner une valeur à R et calculer le périmètre du cercle de rayon R

```
from math import pi

Radius = float(input())
Perimeter = 2 * pi * Radius
print(Perimeter)
```


4 - Ecrire un programme ayant une variable S contenant des secondes. Afficher le nombre d'heures et de minutes correspondantes.

```
Sec = 500
Hour = Sec//3600
Sec = Sec%3600
Min = Sec//60
Sec = Sec%60

print(Hour,Min,Sec)
```
