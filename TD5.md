# TD 5

## Exercice 1

1. Il faut compter tous les éléments groupés par années et accéder à tous les champs années. Donc un scan est suffisant.
2. L'index non groupant fait la même chose.
3. Un index trié sur l'année.
4. t
   - On fait l'index sur l'année car : suppose que le pourcentage de films de 2017 est faible par rapport au nombre total de films.
   - Type 2
   - Bit map index scan et heap sca, pour éviter de recharger des pages si l'index n'est pas groupant.

## Exercice 2
1. 40 enregistrements par page
2. t
   1. 50000 ($\frac{50000}{400000} = 12.5$%)
   2. 1
   3. 19
   4. 399999
   5. 20000
   6. 100000
3. Pour un scan, 10000 pages chargées ($\frac{400000}{40} = 10000$ pages)
4. t
   1. 50000/500 = 100 accès feuilles

        accès table = 50000/40 = 1250

        Total = 4 + 100 + 1250 = 1354   

        (Le 4 est relatif à la hauteur + 1. C'est le coût de descente dans l'arbre)  
   2. Coût accès feuille : 4, parcours des feuilles : 100

        Coût chargement table : Dans le pire des cas, on charge une page différente à chaque fois, donc 50000 pages.

        Coût tôtal : 50104


