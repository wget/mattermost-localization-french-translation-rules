# Règles pour la traduction francophone de Mattermost


## Introduction

Bonjour et merci de participer à la traduction francophone de Mattermost !

Mattermost utilise [une instance Pootle pour ses traductions](http://translate.mattermost.com/fr/). Si ce n'est pas déjà fait, veuillez créer une compte sur cette instance pour pouvoir participer.

De même, il est vivement recommandé d'[utiliser une version de développement de Mattermost](https://docs.mattermost.com/developer/developer-setup.html) de façon à pouvoir vous [assurer que vos traductions soient correctes selon le contexte](https://docs.mattermost.com/developer/localization-process.html#test-translations).

Enfin, veuillez prendre la peine de lire ces quelques règles de traduction à respecter.

Le nombre de chaînes à traduire étant assez élevé au sein du projet Mattermost, si vous trouvez des traductions qui ne respectent pas ces quelques règles, merci de proposer une correction dans l'[interface Pootle de traduction](http://translate.mattermost.com/fr/).

Si vous ne trouvez pas comment traduire un terme, regardez comment le même terme a été traduit les fois précédentes, ou posez votre question sur [le canal Mattermost de traduction francophone](https://pre-release.mattermost.com/core/channels/french-localization).

## Style

### Usage de l'impératif

> Enter your credentials

ne se traduira jamais directement par

> Saisissez vos informations d'identification

mais par

> **Veuillez** saisir vos informations d'identification


### Majuscules

Les anglophones apprécient placer des majuscules dans des mots qu'ils considèrent composés, ex.: 

> System Console


> Private Messages

En français, nous n'utilisons pas de majuscules.

> Console **s**ystème


> Messages **p**rivés


### Abbréviations

Exemple s'agrège en `ex. :`. Notez l'utilisation d'un espace après le point. Bien que vous devriez utiliser une espace insécable, le fait que son insertion [soit assez difficile](https://fr.wikipedia.org/wiki/Espace_ins%C3%A9cable#.C3.80_la_saisie) et que que son utilisation n'ait pas encore été testée au sein de Mattermost, l'utilisation d'espaces simples est recommandée, du moins, pour l'instant.

### Guillemets

Utilisez simplement les guillemets anglophones (`"hello world"`) pour l'instant. Ici aussi, insérer des guillemets francophones dans un formulaire HTML est assez compliqué et leur utilisation n'a pas non plus été testée dans l'interface de Mattermost.


### Traduction trop longues

Si votre traduction s'avère être trop longue pour l'espace que l'interface utilisateur occroie et si compte tenu du sens, vous n'êtes pas en mesure d'aggréger la traduction francophone, veuillez exposer le problème sur le [canal "Localization" de Mattermost](https://pre-release.mattermost.com/core/channels/localization).


## Vocabulaire


### Enter / specify

Ceci dépend du contexte, si on initialise un champ pour la première fois, 
on utilise `spécifier`, si on doit introduire ses identifiants, c'est `saisir`.

> Please enter your email

se traduira par

> Veuillez **saisir** votre adresse e-mail

---

> Please enter an email address

se traduira par

> Veuillez **spécifier** une adresse e-mail


### Email

Utilisez `adresse e-mail` et non `adresse électronique`. `Adresse électronique` n'a jamais vraiment été utilisé en dehors
de la France et tend à être rendu nébuleux à cause des protocoles récents tels que le Bitcoin
ou la Blockchain qui, eux, utilisent une adresse électronique.


### Flag

| EN | FR |
| --- | --- |
| Flagged Posts | Messages marqués d'un indicateur |
| Flag | Marquer avec un indicateur |
| Flag | Ajouter un indicateur |
| Flag | Marquer |
| Unflag | Supprimer l'indicateur |

Remarquons que plusieurs traductions pour `flag` ont été utilisées ci-dessus. Choisissez simplement celle qui convient en fonction de la taille disponible.


### Follow up

Il s'agit simplement des indicateurs pour suivre un message. 

| EN | FR |
| --- | --- |
| Follow up flag | Indicateur de suivi |


### Routes

Bien que ces messages devraient être principalement être vus par du personnel technique et donc sachant parler anglais, il est toutefois préférable de les traduire.

> Initializing team API routes

se traduira par

> Initialisation des routes de l'API équipe

Il faut voir une API comme un arbre ou chaque branche est appelée `route` et chaque embranchement (y compris le tout dernier placé en feuille) est appelé un `noeud`.

Microsoft, dans le cadre de sa plateforme .NET, possède une des rares documentations techniques traduite intégralement en français. Dans le cas qui nous préoccupe, un [article en anglais](https://msdn.microsoft.com/en-us//library/cc668201(v=vs.100).aspx) dispose d'[une correspondance française](https://msdn.microsoft.com/en-us//library/cc668201(v=vs.100).aspx).

On n'utilise le terme `routage` que dans ce cas-ci :

> ASP.NET Routing

se traduira par

> Routage ASP.NET

---

Pour tout le reste, Microsoft utilise au choix : `route` ou `itinéraire`. Dans le cas de Mattermost, de façon à uniformiser les traductions, et se rapprocher de la version anglophone, nous utiliserons le terme `route`.

---

De même, toujours basé sur l'exemple `Initializing team API routes`, nous n'utilisons pas de pluriel pour qualifier le noeud, ni nous n'utilisons de prépositions de lien.

Les propositions suivantes sont donc invalides et seront refusées dans Mattermost:

> Initialisation des routes de l'API d'équipe

> Initialisation des routes de l'API des équipes

> Initialisation des routes des APIs d'équipes

> Initialisation des routes des APIs de l'équipe


### Slash commands

Il s'agit des commandes que vous saisissez lorsque vous commencez votre message par un slash dans Mattermost. La décision a été de traduire ce terme par `commandes slash`.


### Token / secret key

* `Token`: Utilisez le mot `jeton` à la place.
* `Secret key`: Clé secrète si c'est une clé utilisée dans le sens clé à ne pas divulguer, clé privée dans le cas où il est fait mention de clé publique ou s'il est question de chiffrement asymétrique.


### Trigger

> A trigger word cannot begin with a /

se traduira par

> Un mot**-clé** déclencheur ne peut commencer par un /

