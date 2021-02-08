1 - Créer une fonction qui prend en paramètre un chiffre X et qui affiche X fois ‘coucou’ via une fonction récursive 

```
def rec_coucou(nb_coucou):
  if nb_coucou > 0:
    print("Coucou")
    rec_coucou(nb_coucou-1)
```

2 - Recréer la fonction calculant la puissance via une fonction récursive

```
def rec_pow(number,power):
  if power<=0:
    return 1
  return number * rec_pow(number,power-1)
```

3 - Calculer la factorielle d’un nombre via une fonction récursive

```
def rec_fact(X):
  if X <= 1:
    return 1
  return X*rec_fact(X-1)
```


4 - Refaire l'exercice sur la suite de fibonacci via une fonction récursive

```
def Fibo(X):
  if X<=1:
    return X
  return Fibo(X-1) + Fibo(X-2)
```

```
cache=[0,1]

def fib(n):
  if n<len(cache):
    return cache[n] 
  else :
      calcul = fib(n-1) + fib(n-2) 
      cache.append(calcul) 
      return calcul

print(fib(5))
```

5 - Refaire l'exercice sur le calcul du pgcd via une fonction recursive

```
def rec_pgcd(a,b):
  if a%b==0:
    return b
  return rec_pgcd(b,a%b)
```

6 - Créer une fonction récursive permettant de retourner une chaine de charactères ("coucou" devient "uocuoc")

```
txt = "coucou" #-> uocuoc

def reverse_string (txt) :
  if len(txt) > 0:
    return txt[-1] + reverse_string(txt[:-1])
  else:
    return ""

print(reverse_string("coucou"))

#"u" + reverse("couco")
#"u" + "o" + reverse("couc")
#"u" + "o" + "c" + reverse("cou")
#"u" + "o" + "c" + "u" + reverse("co")
#"u" + "o" + "c" + "u" + "o" + reverse("c")
#"u" + "o" + "c" + "u" + "o" + "c" + reverse("")
#"u" + "o" + "c" + "u" + "o" + "c" + ""
```
