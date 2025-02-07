# whoisloggedin

## Description
`whoisloggedin` est un projet qui permet de savoir quels utilisateurs sont actuellement connectés au réseau de l'Institut Claude Chappe au sein de la Faculté des Sciences & Techniques de l'Université du Mans. Il utilise des commandes système pour récupérer et afficher les informations des utilisateurs connectés.

## Fonctionnalités
- Affiche la liste des ordianteurs actuellement allumés
- Affiche la liste des utilisateurs actuellement connectés

## Prérequis
- Accès à un compte étudiant de l'Université du Mans
- Accès à un session utilisateur en licence informatique au sein de l'Institut Claude Chappe
- Listes d'associations entre un identifiant d'étudiant (numéro INE) et le nom des étudiants

### Comment se procurer ces listes

Plusieurs options s'offrent à vous pour obtenir ces listes :
- Les modules UMTICE "d'informations générales" où chaque étudiant de l'établissement est inscrit automatiquement. Il faut ainsi récupérer la liste des inscrits à la licence en question. Cette liste contient généralement leur nom associé à un grand nombre correspondant à l'identifiant recherché.
- Les résultats d'examen reçus par messagerie qui contiennent parfois les fameuses associations.

Il faut télécharger ces fichiers, ceux-ci étant généralement au format PDF, ou copier leur contenu (Ctrl-A puis Ctrl-C).

Lorsque vous avez réussi à obtenir le fichier, demandez à ChatGPT ou un autre modèle d'intelligence artificielle de vous le formater (en l'important ou en collant son contenu) à l'aide de ce prompt :

```
Mon pote, j'ai besoin que tu me formates ce que je viens de te passer de sorte à avoir une liste d'identifiants, de grands nombres, et de noms puis prénoms, tous en majuscules et espacés, dans ce style : 
23001379 DUPONT JEAN-PIERRE
```
L'objectif est d'avoir une liste pour chaque niveau. Les listes d'étudiants en L1, L2 et L3 informatique doivent être dans des fichiers respectivement et rigoureusement nommés `id_l1.txt`, `id_l2.txt` et `id_l3.txt`. Ces fichiers doivent être placés dans le dossier `whoisloggedin`.

## Installation
Clonez le dépôt et accédez au répertoire du projet :
```bash
git clone https://github.com/votre-utilisateur/whoisloggedin.git
cd whoisloggedin
```

Lancez la configuration :
```bash
./configure
```

## Utilisation
Exécutez le script principal pour afficher les utilisateurs connectés :
```bash
./audit_pc -o | ./whoisloggedin -u
```

Le programme de fonctionnera pas sans les listes des noms/identifiants d'étudiant.

## Contribuer
Les contributions sont les bienvenues ! Veuillez soumettre une pull request ou ouvrir une issue pour discuter des changements que vous souhaitez apporter.

## Licence
Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## Auteurs
- Patrick PASTOURET - Créateur et développeur principal
