# Linux


**TP challenges**
---

**Le premier:**

Le fichier /etc/passwd défini les utilisateurs, le 4ieme champ contien l'id de groupe le gid.
Trouvez, en une seule ligne de commande utilisant des filtres combinés, quel est le gid le plus utilisé.

Réponse: `id -g sync`


**Le deuz':**

Le fichier /etc/group defini les groupes connu du système
dans une ligne de commande on peu substitué une partie de la ligne de commande par le résultat d'une ligne commande $(commande)

Exemple:
        `echo mon uid est $(grep alan /etc/passwd | cut -d: -f3 | head -1)`
        
En utilisant ceci et la réponse à la première question, affichez en une seule commande le nom du groupe associé au gid le plus utilisé

Réponse: `......`
