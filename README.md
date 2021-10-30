# TP4: Bibliothèques scientifiques et graphiques | Tests et outils de correction

- [Directives particulières](#directives-particuli%C3%A8res)
- [Objectifs](#objectifs)
- [Partie 1: Exploration de la base de données](#partie-1-Lire-et-construire-la-base-de-donn%C3%A9es)
- [Partie 2: Affichage graphique des données](#partie-2-analyse-des-donn%C3%A9es)
- [Partie 3: Rédaction des tests](#partie-3-rédactions-des-tests)

:alarm_clock: [Date de remise le dimanche 14 novembre à 23h59](https://www.timeanddate.com/countdown/generic?iso=20210406T2359&p0=165&font=cursive)

## Directives particulières
* Un fichier TP4.ipynb sera utilisé;
* Il suffit de faire un 'pip install jupyter' puis de rajouter jupyter sur pycharm afin de l'ouvrir, les jupyter notebook sont intéressants pour leur affichage rapide et vous familiariserons avec un outil communément utilisé;
* N'oubliez pas également d'installer les librairies manquantes (seaborn, numpy et pandas) via anaconda ou directement via pycharm; 
* Pas de librairies externes autres que celles déjà importées.

## Objectifs
Le TP4 se concentre sur l'utilisation de librairies scientifiques et graphiques. Plus précisément, vous aurez à vous familiariser avec numpy et pandas, des librairies essentielles en python en plus de visualiser certaines données avec matplotlib et seaborn. Exceptionnellement, les étapes à suivre pour les parties 1 et 2 seront expliquées entièrement dans le jupyter notebook nommé TP4.ipynb. Pour ce qui est de la partie 3 sur la rédaction de tests, un élément important lors de la réalisation de projet en programmation, les instructions sont ci-dessous.

## Partie 3: Rédactions des tests
Comme vu en classe, il est très important de tester extensivement le code écrit. C'est malheureusement une pratique souvent ignorée par manque de temps ou d'intérêt. Mais comme pour toute autre bonne pratique en génie informatique/logiciel, les conséquences négatives d'une telle décision finissent par nous rattraper tous.

Dans le cas spécifique d'un jeu, qui dépend d'une interaction constante entre le joueur et la logique de jeu (à travers les commandes), les tests sont encore plus importants. Il vous sera donc demandé de tester l'ensemble des fonctions définies dans *logique.py*

Le fichier *tests.py* contient un exemple de code rédigé pour tester UN cas d'utilisation d'UNE fonction (à noter que le test en tant que tel n'est pas implémenté). De plus, vous devez rajouter l'appel aux tests que vous ajoutez dans le *main* de la même façon que pour l'exemple.
```python
# Tests 
def tester_inverser_matrice_identite():
    matrice = [[1, 0, 0, 0],
               [0, 1, 0, 0],
               [0, 0, 1, 0],
               [0, 0, 0, 1]]
    matrice_attendue = [[0, 0, 0, 1],
                        [0, 0, 1, 0],
                        [0, 1, 0, 0],
                        [1, 0, 0, 0]]
    return logique.inverser(matrice) == matrice_attendue

# Affichage des tests
def ecrire_resultat_test(test, resultat):
    reussite_ou_echec = ("Échec", "Réussite")[resultat]
    print(test + "..." + reussite_ou_echec)


if __name__ == '__main__':
    ecrire_resultat_test(tester_inverser_matrice_identite.__name__, tester_inverser_matrice_identite())
```

### À faire

Votre code doit tester les cas (valeurs d'entrées et d'exécutions) **limites** des fonctions afin de repérer d'éventuelles erreurs de logique. Une fonction par cas de test vous est demandé. Normalement, pour avoir une couverture exhaustive du code, il faut s'assurer de passer par tous les chemins de code ainsi que par toutes les valeurs limites. Toutefois, pour ce TP, 2 cas de tests par fonction sera suffisant. Veuillez vous assurer d'avoir un nom clair qui identifie bien la fonction testée ainsi que le cas de test.  
**Puisque la fonction initialiser_nouvelle_matrice() ne prend pas de paramètres et qu'elle retourne toujours la même chose, un seul test est nécessaire.**

Exemple: Tests pour la fonction inverser
* tester_inverser_matrice_identite()
* tester_inverser_matrice_remplie()


