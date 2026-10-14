Alexis MAFFRE

| Étape/version testée | Action | Résultat attendu | Résultat constaté |
| Étape 1 | Actualiser la page | Fond bleu nuit et texte blanc | Réussi |
| Étape 1 | Tester en largeur 390 px | Aucun débordement horizontal | Réussi |
| Étape 2 | Ouvrir le site | Confirmation cachée | Réussi |
| Étape 2 | Cliquer 1 fois sur Réserver | Confirmation visible, 1 place | Réussi |
| Étape 2 | Cliquer 2 fois de plus | Confirmation actualisée, 3 places | Réussi |
| Étape 2 | Cliquer sur Recommencer | Compteur à 0, confirmation cachée | Réussi |
| Étape 3 | Fusionner les branches A et B | Thème sombre et confirmation actifs | Réussi |
| Étape 4 | Vérifier la confirmation avant correction | Identifier si le message est lisible | Réussi |
| Étape 4 | Modifier le CSS de la confirmation | Message mieux visible avec un encadré | Réussi |
| Étape 5 | Réserver une place | Nom de l'atelier affiché, 1 place | Réussi |
| Étape 5 | Réserver 3 places | Nom de l'atelier affiché, 3 places | Réussi |
| Étape 6 | Actualiser le site | Compteur à 0, confirmation cachée | Réussi |
| Étape 6 | Réserver une place | Compteur à 1, confirmation lisible | Réussi |
| Étape 6 | Réserver 3 places | Compteur et confirmation à 3 | Réussi |
| Étape 6 | Cliquer sur Recommencer | Compteur à 0, confirmation cachée | Réussi |
| Étape 6 | Réserver après remise à zéro | Compteur à 1, confirmation visible | Réussi |
| Étape 6 | Tester en largeur 390 px | Aucun débordement, boutons lisibles | Réussi |


Aides utilisé pour le terminal j'ai cherché ces commandes: avec Chat gpt
Je lui ai demandé pour bien vérifier le système branche qu'est ce que je pourrais faire
git rev-parse HEAD	
git rev-parse "depart-cc^{commit}"		
git log --oneline --graph --all
Pour trouver le commit de départ 
git merge-base feature/theme-sombre feature/confirmation

Base et branches

Le commit commun aux branches A et B est 67aeb4f depart-cc.

La branche hotfix a été créée après la fusion de A et B, et la quatrième branche après le commit 197c9bb du hotfix.

Fusion et fonctionnement

Une fusion Git réussie ne garantit pas que le site fonctionne, il ne vérifie pas l'affichage.

Dans mon projet, la confirmation était difficile à lire avec le thème sombre. J'ai donc amélioré son contraste avec un fond bleu, un texte blanc.

Commit et publication :

Après un commit local, il faut utiliser git push pour publier les modifications sur GitHub.

Mon commit 1047243 correspond à l'ajout du nom de l'atelier dans la confirmation. Je l'ai vérifier dans l'historique des commits de main sur GitHub.
