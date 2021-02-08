1 - Créer une fonction qui répond oui ou non au fait que le paramètre donné soit un chiffre premier ou pas

```
def IsPrimeNumber(number):
  i = 2
  while i*i <= number:
    if number%i == 0:
      return False
    i += 1
  return True


if IsPrimeNumber(113):
  print("Coucou")
```

2 - Créer une fonction qui prend en paramètre un chiffre et qui affiche tout les chiffres premiers inférieur au paramètre

```
def PrintPrimeNumberUnderLimit (limit):
  i = 2
  while i < limit:
    if IsPrimeNumber(i):
      print(i)
    i += 1
  
PrintPrimeNumberUnderLimit(1000)
```

3 - Ecrire une fonction simulant un lancé de dé à 6 faces

```
from random import randint

def DiceThrow():
  return randint(1,6)

print(DiceThrow())
```

4 - faire un jeu à base de lancé de dés, le but est de faire, avec 3 dés une combinaison de trois fois la même valeur.
Pour cela il est possible de relancer jusqu'à 3 fois certains dès si leurs valeurs ne nous conviennent pas.

```
def DoIneedToReroll(D):
  print("Voulez vous relancer le dé",D,"y/n :")
  User_choice = input()
  return User_choice == "y"

def PlayerHasWin(D1,D2,D3):
  return D1 == D2 == D3

def DiceGame():
  D1 = DiceThrow()
  D2 = DiceThrow()
  D3 = DiceThrow()
  print(D1,D2,D3)

  Roll_counter = 0

  while not PlayerHasWin(D1,D2,D3) and Roll_counter < 3:
    if DoIneedToReroll(1):
      D1 = DiceThrow()  

    if DoIneedToReroll(2):
      D2 = DiceThrow() 

    if DoIneedToReroll(3):
      D3 = DiceThrow() 

    Roll_counter += 1
    print(D1,D2,D3)

  if PlayerHasWin(D1,D2,D3):
    print("Victoire")
  else:
    print("Défaite")

DiceGame()
```

5 - Créer une fonction trouvant le PGCD d'un nombre

```
def Pgcd (V1, V2):
# x -> PGCD
# V1%x==0 and V2%x==0
  pgcd = 1
  i = 2

  while i<=V1 and i<=V2:
    if V1%i==0 and V2%i==0:
      pgcd = i
    i+=1
  return pgcd

print(Pgcd(50,100))
```

```
def Pgcd2 (V1, V2):
  
  i = Min(V1,V2)
  while i > 1:
    if V1%i==0 and V2%i==0:
      return i
    i-=1
  return 1

print(Pgcd(30,20))
```

```
def pgcd3(a,b) :  
   while a%b != 0 : 
      a, b = b, a%b 
   return b

print(pgcd3(100,28))
```


6 - Créer une simulation de combat entre un joueur et un monstre, le joueur possède des vies et le monstre aussi, le combat se déroule en tour par tour, à chaque fois on propose au joueur plusieurs attaques différentes infligeant plus ou moins de dégats et en retour le monstre contre attaque. La fonction renvoie si oui ou non le combat a été gagné par le joueur.

```
from random import randint

def Damage(basic_attack, heavy_attack):
  amount_damage = 0
  NextMove = input('Que voulez vous faire ? 1 => Attaque Basique, 2=> Attaque Lourde')
  if (NextMove == '1'): 
    amount_damage = basic_attack
  elif (NextMove == '2'):
    dice = randint(1,100)
    if dice <= 70:
      print('Attaque lourde réussie')
      amount_damage = heavy_attack
    else:
      print('Coup manqué')
  return amount_damage

def combat():
  PlayerHealth = 100
  BasicAttack = 15
  HeavyAttack = 25

  EnnemyHealth = 150
  EnnemyAttack = 10

  while PlayerHealth > 0 and EnnemyHealth > 0:
    print('Votre vie : ')
    print(PlayerHealth)
    print('Vie de l\'ennemi : ')
    print(EnnemyHealth)

    EnnemyHealth -= Damage(BasicAttack,HeavyAttack)
    PlayerHealth -= EnnemyAttack

  if (PlayerHealth <= 0):
    print('Vous êtes mort')
  else:
    print('L\'ennemi est mort, bravo !')

combat()
```
