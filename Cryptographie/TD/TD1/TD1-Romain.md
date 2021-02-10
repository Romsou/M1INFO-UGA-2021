# Exercice 1

## Q1 

```
ThrowEggs():
    height = 0;
    Max_Height = 100;
    while(egg.isNotBroken() && height++ < Max_Height):
        Climb(height);
        egg.throw(height);
    return height =< max_height ? return height: return -1;
```

```
beg = 0;
end = 100;
ThrowEggsDichotomy(beg, end):
    middle = (beg + end) / 2
    egg.throw(middle)
    if (egg.isBroken()):
        return middle;

    ThrowEggsDichotomy(beg, middle);
    ThrowEggsDichotomy(middle + 1, end);
```
        
Solution pour l'algo en racine de N:

```
i = sqrt(n)
Tant que i <= N faire
  Lancer_oeuf(i)
  Si oeuf cassé alors
    j = i - sqrt(n)
    Tant que j <= i faire
      j += 1
      Lancer_oeuf(j)
      Si oeuf cassé alors
        Renvoyer j
  Sinon
    i += sqrt(n)
Renvoyer N
```

$P[x \oplus r] 
\\ = P[(x \land \lnot r) \lor (\lnot x \land r)] 
\\ = P[{0, 1}] + P[{1, 0}] 
\\ = (p * 1/2) + ((1- p) * 1/2) 
\\ = (p + 1 - p) / 2 
\\ = 1/2 ?$

Q.1bis: ça n'a rien changé
$P[x \oplus r = 0 | x = 0] = P[r]$

Q3.1 Il faut que k soit tiré uniformément.

**Note:** faire attention au nombre de bit de p, p' et k. k s'applique à p et p' car il fait la bonne taille pour eux, donc on ne peut pas faire p||p' Xor k

Probabilité de tirer une chaîne 2^n bit similaire à notre chaîne de taille n concaténé:
ensemble des chaines de taille 2n = 2^(2n) du coup proba = 2^n / 2^(2n)

## Exercice 3

Q.1 $\frac{1}{N^2}$

Q.2 $P[X = Y] = Sum_{x \in S} P[X = x] et P[Y = x | sachant que X = x] = P[X = Y] = Sum_{x \in S} P[X = x]*P[Y = x] = 1 / N$
Deuxième solution: C'est un tirage aléatoire avec remise parmis N possibilités, on peut donc se dire qu'on tire une variable parmis N possibilité, puis
qu'on tire parmis N possiblités une valeur qui a 1/N d'être égale à la précédente, soit 1/N chances d'avoir X = Y.

Q.3 1 / N^2

## Exercice 4

Q.1 7, 6 et non car certains élements n'ont pas d'inverses.

Q.2 5,  

Q.3 Dans l'ordre: Pas un corps, un corps, Un corps car 7 premier, pas un corps
