# TD6

## Exercice 1

R : 3 pages ; 5 enregistrements<br>
S : 3 pages ; 6 enregistrements

1. a2,a5<br>
   a2,a6<br>
   a2,a1<br>
   a2,a2 -> M<br>
   ...<br>
   a1,a2

   Coût : $3 + 5 \times 3 = 18$

2. Pages à pages
   Coût
   $3+3\times 3 = 12$

3. Paquet
   $3+2\times 2 = 7$
4. $3 + 5 \times (1+5) = 33$
5. $3+3$ (car les listes étant triées, on ne parcourt chaque liste qu'une fois)

## Exercice 2

R : 1000 pages ; 10000 enregistrements<br>
S : 200 pages  ; 2000 enregistrements

1. ### Pages à page
   $1000 + 200 \times 1000 = 201000$<br>
   $200 + 1000 \times 200 = 200200$

   Bien que les deux réponses soient correctes, le second calcul est moins cher.

   Taille buffer minimum : 3 (car au moins un espace pour R, un pour S, et un pour le résultat)

2. ### Paquets
   $200 + \frac{100}{52 - 2} * 1000 = 4200$ (on retire 2 pour le résultat et T1)
3. ### tri-fusion
   `math.log(200,51)` (pour calculer un log en python ; ici $log_{51}(200)$)

   Coût du build :<br>
   $2 \times 200 \times log_{51}(200) + 2 \times 1000 \times log_{51}(1000)$<br>
   $2 \times 200 \times 2 + 2 \times 1000 \times 2 = 800 + 4000 = 4800$<br>

   Coût du probe :<br>
   $1000 + 200 = 1200$
   
   Coût total : <br>
   $4800 + 1200 = 6000$


   $32 \times 32 = 1024$ (supérieur à 100)<br>
   Donc taille minimale = 32 + 1 (car il faut prendre en compte le res)
   
4. ### Hashage
   Création tables<br>
   $2 \times FT1 + 2 \times FT2$<br>
   $2 \times 200 + 2 \times 1000 = 2400$

   Jointure<br>
   $FT_1+FT_2$~<br>
   $200 + 1000 = 1200$

   Total<br>
   $2400 + 1200 = 3600$

5. Par paquets avec un buffer de taille 202 
   
   $FT_1 + \frac{FT_1}{200} \times FT_2$<br>
   $200 + \frac{200}{200} \times 1000$<br>
   $200 + 1 \times 1000 = 1200$

6. Pire des cas <br>
   - avec lenombre d'enregistrements de la plus grande table, ici R : 10000
   - Coût d'e/p : 5<br>
   
    En tout : $\frac{10000}{5} = 2000$ pages 