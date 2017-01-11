Tous les traducteurs francophones doivent se soumettre à ces quelques règles de traduction.

Le nombre de châines à traduire étant particulièrement grand au sein de Mattermost, si vous trouvez des traductions qui ne respectent pas ces quelques règles, merci de proposer une correction dans [l'interface Pootle de traduction](http://translate.mattermost.com/fr/).

# Style

## Usage de l'impératif

> Enter your credentials

ne se traduira jamais directement par

> Saisissez vos informations d'identification

mais par

> **Veuillez** saisir vos informations d'identification

# Traductions

## Enter / specify

Ceci dépend du contexte, si on initialise un champ pour la première fois, 
on utilise `spécifier`, si on doit introduire ses identifiants, c'est `saisir`.

> Please enter your email

se traduira par

> Veuillez **saisir** votre adresse e-mail

---

> Please enter an email address

se traduira par

> Veuillez **spécifier** une adresse e-mail

## Token / secret key

* `Token`: Utilisez le mot `jeton` à la place.
* `Secret key`: Clé secrète si c'est une clé utilisée dans le sens clé à ne pas divulguer, clé privée dans le cas où il est fait mention de clé publique ou s'il est question de chiffrement asymétrique.

## Email address

Utilisez `adresse e-mail` et non `adresse électronique`. `Adresse électronique` n'a jamais vraiment été utilisé en dehors
de la France et tend à être rendu nébuleux à cause des protocoles récents tels que le Bitcoin
ou la Blockchain qui, eux, utilisent une adresse électronique.

## Routes

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


## Trigger

> A trigger word cannot begin with a /

se traduira par

> Un mot**-clé** déclencheur ne peut commencer par un /

