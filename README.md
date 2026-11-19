# espace-sondage

> **Espace Grist clé en main.** Un document Grist prêt à l'emploi pour **mener une enquête** : concevoir le questionnaire, savoir qui a répondu et lire tout de suite les résultats en indicateurs, au Système de design de l'État (DSFR).

Un **espace** est un document Grist complet — tables, formules, pages, widgets et réglages — à importer en une fois. Il assemble des widgets de la famille `grist-…` autour d'une manière de travailler. Chaque widget reste utilisable seul.

## À quoi ça sert

- **Concevoir un questionnaire au DSFR** sans code : étapes, questions conditionnelles, choix uniques ou multiples, **notes sur une échelle réglable** (de 1 à 5, de 0 à 10…), commentaire libre.
- **Le diffuser** par un lien public : les personnes répondent sans compte Grist.
- **Savoir qui a répondu** : la table `Destinataires` liste les personnes invitées et indique, pour chacune, si elle a répondu et s'il faut la relancer. Le lien se fait par l'adresse électronique, si la personne l'a donnée.
- **Lire les résultats** : nombre de réponses, taux de réponse, satisfaction moyenne, répartition des notes, résultats par service, derniers commentaires. Les indicateurs se mettent à jour à chaque réponse.

## Ce que contient l'espace

| Page | Outil | Contenu |
| --- | --- | --- |
| **Concevoir le questionnaire** | [grist-questionnaire](https://github.com/lab17bis/grist-questionnaire) | Questions, étapes, conditions, textes, aperçu et publication. |
| **Indicateurs** | [grist-graphique](https://github.com/lab17bis/grist-graphique) | Résultats de l'enquête. Page *Régler les indicateurs* pour les modifier. |
| **Réponses** | tables Grist | Toutes les réponses. Table `Reponses`. |
| **Qui a répondu** | tables Grist | Personnes invitées, réponse reçue ou non, relances. Table `Destinataires`. |

## L'installer en 2 minutes

1. **Télécharger** le fichier de l'espace :
   - [`espace-sondage.grist`](https://github.com/lab17bis/espace-sondage/raw/main/espace-sondage.grist) : l'espace vide, prêt à l'usage ;
   - [`espace-sondage-exemple.grist`](https://github.com/lab17bis/espace-sondage/raw/main/espace-sondage-exemple.grist) : le même, rempli de données fictives, pour essayer.
2. **L'importer dans Grist** : depuis l'accueil de votre espace Grist, *Ajouter › Importer un document*, puis choisissez le fichier.
3. **L'ouvrir** : les pages et les widgets sont déjà en place. Si Grist le demande, confirmez l'accès complet des widgets au document.
4. **Inviter l'équipe** (*Partager*), en éditeur pour celles et ceux qui saisissent.

Vous êtes propriétaire du document importé. Rien n'est installé ailleurs : les widgets sont des pages web publiques, qui lisent et écrivent dans votre document avec les droits de la personne connectée.

Les widgets sont chargés depuis leur **adresse stable** (`…/v1/`) : une évolution d'un widget ne modifie pas votre espace sans que vous l'ayez décidé.

## Le régler

- **Questions** : page *Concevoir le questionnaire*. Une nouvelle question crée sa colonne dans `Reponses`.
- **Échelle de notes** : type de question *Note sur une échelle*, avec la note la plus basse, la plus haute et leur sens.
- **Publication** : onglet *Publication* du questionnaire, qui guide la publication du formulaire Grist et donne le lien à diffuser.
- **Anonymat** : si l'enquête doit être anonyme, supprimez la question sur l'adresse électronique ; la table `Destinataires` ne servira alors qu'à suivre les invitations.
- **Indicateurs** : page *Régler les indicateurs*. Pensez à les adapter quand vous changez les questions.

Les réglages sont enregistrés dans le document. Ils partagent les mêmes réglages d'en-tête et de pied de page.

## Données et droits d'accès

Le lien public du questionnaire permet seulement **d'ajouter** une réponse : il ne donne accès ni aux réponses, ni aux autres tables. Les réponses et la liste des destinataires ne sont visibles que des personnes invitées dans le document.

Les tables `Personnes` et `Structures`, quand l'espace en contient, suivent la règle commune des widgets : un widget de la famille ajouté plus tard les reprend et les complète, au lieu d'en créer d'autres.

Les fichiers de ce dépôt ne contiennent aucune donnée réelle. L'exemple est entièrement fictif.

## Widgets utilisés

- [grist-questionnaire](https://github.com/lab17bis/grist-questionnaire) : questionnaires au DSFR avec logique conditionnelle et notes sur une échelle.
- [grist-graphique](https://github.com/lab17bis/grist-graphique) : tableaux de bord et indicateurs à seuils au DSFR.

## Autres espaces

- [espace-pilotage](https://github.com/lab17bis/espace-pilotage) : regarder et décider : un écran d'équipe qui rassemble indicateurs, réunions, projets et management visuel.
- [espace-collaboratif](https://github.com/lab17bis/espace-collaboratif) : faire ensemble : réunions, projets partagés et ressources communes d'une équipe.
- [espace-accompagnement](https://github.com/lab17bis/espace-accompagnement) : suivre les personnes qui sollicitent un service : offre de service, sollicitations, fiches contact et satisfaction.
- [espace-reseau](https://github.com/lab17bis/espace-reseau) : animer un réseau ou une communauté de pratique : membres, groupes, rencontres, présences, ressources partagées, retours, carte et liens entre acteurs.
- [espace-contributions](https://github.com/lab17bis/espace-contributions) : faire participer : boîte à idées, valorisation des réalisations des équipes, votes et suites données.

## Écosystème

- **[Grist](https://grist.numerique.gouv.fr)** : tableur-base de données libre ([gristlabs/grist-core](https://github.com/gristlabs/grist-core)), proposé aux agents publics par la [DINUM](https://www.numerique.gouv.fr/) dans [La Suite numérique](https://lasuite.numerique.gouv.fr/). L'espace s'importe dans toute instance de Grist.
- **[Système de design de l'État (DSFR)](https://www.systeme-de-design.gouv.fr/)** ([GouvernementFR/dsfr](https://github.com/GouvernementFR/dsfr)). Son usage est réservé aux sites des services de l'État.

## Mots-clés

Grist, espace Grist, modèle Grist, document clé en main, sondage, enquête, questionnaire, formulaire, enquête de satisfaction, échelle de notes, taux de réponse, relance, indicateurs, tableau de bord, DSFR, Système de design de l'État, La Suite numérique, service public, logiciel libre.

## Licence

Fichiers de l'espace et documentation sous licence Creative Commons [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.fr) : réutilisation et adaptation autorisées, en citant la source et en partageant sous la même licence. Le code des widgets est sous licence MIT, dans leurs dépôts.

Conçu par le Lab 17 bis, laboratoire d'innovation publique de l'académie de Reims. Contact : <lab17bis@ac-reims.fr>
