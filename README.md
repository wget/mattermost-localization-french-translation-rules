# Règles pour la traduction francophone de Mattermost

<!-- vim-markdown-toc GFM -->
* [Introduction](#introduction)
* [Style](#style)
    * [Jargon](#jargon)
    * [Usage de l'impératif](#usage-de-limpératif)
    * [Usage du futur simple](#usage-du-futur-simple)
    * [Majuscules](#majuscules)
    * [Abbréviations](#abbréviations)
    * [Guillemets](#guillemets)
    * [Pluriel de majesté (We couldn't...)](#pluriel-de-majesté-we-couldnt)
    * [Traduction trop longue](#traduction-trop-longue)
    * [Gestion du pluriel](#gestion-du-pluriel)
* [Outils pour le traducteur](#outils-pour-le-traducteur)
* [Vocabulaire](#vocabulaire)
    * [Attach](#attach)
    * [Batch](#batch)
    * [BG](#bg)
    * [Direct](#direct)
    * [Enter / specify / input field](#enter--specify--input-field)
    * [Email](#email)
    * [Emoji](#emoji)
    * [Endpoint](#endpoint)
    * [FileInfos](#fileinfos)
    * [Flag](#flag)
    * [Follow up](#follow-up)
    * [Get](#get)
    * [Hours / timezone](#hours--timezone)
    * [Jobs](#jobs)
    * [Notifications push / mobile / desktop](#notifications-push--mobile--desktop)
    * [Permissions](#permissions)
    * [Posted / posts / publication](#posted--posts--publication)
    * [Private message](#private-message)
    * [Purpose](#purpose)
    * [Rate limits](#rate-limits)
    * [Routes](#routes)
    * [Slash commands](#slash-commands)
    * [SSO](#sso)
    * [Token / secret key](#token--secret-key)
    * [Trigger](#trigger)

<!-- vim-markdown-toc -->

## Introduction

Bonjour et merci de participer à la traduction francophone de Mattermost !

Mattermost utilise [une instance Pootle pour ses traductions](http://translate.mattermost.com/fr/). Si ce n'est pas déjà fait, veuillez créer une compte sur cette instance pour pouvoir participer.

De même, il est vivement recommandé d'[utiliser une version de développement de Mattermost](https://docs.mattermost.com/developer/developer-setup.html) de façon à pouvoir vous [assurer que vos traductions soient correctes selon le contexte](https://docs.mattermost.com/developer/localization-process.html#test-translations).

Enfin, veuillez prendre la peine de lire ces quelques règles de traduction à respecter.

Le nombre de chaînes à traduire étant assez élevé au sein du projet Mattermost, si vous trouvez des traductions qui ne respectent pas ces quelques règles, merci de proposer une correction dans l'[interface Pootle de traduction](http://translate.mattermost.com/fr/).

Si vous ne trouvez pas comment traduire un terme, regardez comment le même terme a été traduit les fois précédentes, regardez sur l'[ancien glossaire créé par Sun](https://glossaire.traduc.org), ou posez votre question sur [le canal Mattermost de traduction francophone](https://pre-release.mattermost.com/core/channels/french-localization).

## Style

### Jargon

Mattermost est utilisé pour envoyer des `messages`. Ces messages peuvent être composés de texte et/ou d'objets tels que des fichiers (images, documents, émoticônes, etc.).

Mattermost distingue 2 types de messages:

* les publications qui sont les messages parents qui débutent un fil de discussion;
* les réponses qui sont les messages répondant à un message parent (publication) dans un fil de discusion.

Si un utilisateur répond à un message sans passer par la fonctionalité de fil de discusion dans la barre latérale de droite, son message sera considéré comme une publication et ouvrira un nouveau fil.

On `envoie` un message et on `publie` une publication.

On `compose` un message, une publication ou une réponse.

cf. [Posted / posts / publication](#posted--posts--publication)

### Usage de l'impératif

| EN | FR |
| --- | --- |
| Enter your credentials | **Veuillez** saisir vos informations d'identification |

De façon à assouplir l'ordre, nous utiliserons `vouloir` à l'impératif avant le verbe représentant l'action à effectuer; pas de mention `s'il vous plait`.

### Usage du futur simple

| EN | FR |
| --- | --- |
| When true, the OAuth 2.0 application is considered trusted by the Mattermost server | Lorsqu'activé, l'application OAuth 2.0 est considérée comme étant de confiance par le serveur | 
| The URL for the About link on the Mattermost login and sign-up pages. If this field is empty, the About link is hidden from users. | L'URL vers la page À propos apparaissant sur les pages de connexion et d'enregistrement de Mattermost. Si ce champ est laissé vide, le lien sera masqué pour les utilisateurs. |
| Slack Import: Channel {{.ChannelName}} header exceeds the maximum length. It will be truncated when imported. | Importateur Slack : L'entête du canal {{.ChannelName}} excède la longueur maximale. Il sera tronqué lors de l'importation. |
| (Optional) The attribute in the AD/LDAP server that will be used to populate the first name of users in Mattermost. When set, users will not be able to edit their first name, since it is synchronized with the LDAP server. When left blank, users can set their own first name in Account Settings. | (Optionnel) L'attribut dans le serveur AD/LDAP qui est utilisé pour les prénoms des utilisateurs de Mattermost. Lorsque défini, les utilisateurs ne peuvent pas éditer leur prénom étant donné qu'il est alors synchronisé avec le serveur LDAP. Lorsque laissé vide, les utilisateurs peuvent définir leur propre prénom dans les paramètres du compte. |

Ne vous calquez pas sur le temps utilisé dans la version anglaise. [Selon une petite étude menée avec des francophones natifs](https://irc.died.re/2017/08/12/#line-536), utiliser l'indicatif futur simple donne l’impression d’une fonctionnalité documentée mais pas encore implémentée.

L'indicatif présent (ici à la voix passive) sonne plus naturellement et semble moins étrange. L'important est ici encore de garder une certaine cohérence. Notre traduction utilise le plus possible de l'indicatif présent; utiliser un temps passé ou futur est, la plupart du temps, à proscrire.

Dans tous les cas, veuillez conserver une concordance des temps correcte. [Pour rappel](https://www.francaisfacile.com/exercices/exercice-francais-2/exercice-francais-15267.php):

* si + présent -> futur simple (ou présent) =>Si tu veux, je viendrai / je viens. (selon le contexte)

* si + imparfait -> conditionnel présent => Si tu voulais, tu pourrais.

* si + plus-que-parfait -> conditionnel passé => Si tu avais voulu, tu aurais pu.

### Majuscules

| EN | FR |
| --- | --- |
| System Console |Console **s**ystème |
| Private Messages | Messages **p**rivés |
| Please configure your {docsLink} in the System Console or in gitlab.rb if you're using GitLab Mattermost. | Veuillez configurer votre {docsLink} dans la console système ou dans le fichier gitlab.rb si vous utilisez GitLab Mattermost. |

Les anglophones apprécient placer des majuscules dans des mots qu'ils considèrent composés. En français, nous n'utilisons pas de majuscules.

De même, en plein milieu d'une phrase de description de fonctionnalité, comme `Aller dans la console système`, nous ne plaçons pas de majuscules. Nous en plaçons uniquement lorsque nous spécifions les menus.

### Abbréviations

Exemple s'agrège en `ex. :`. Notez l'utilisation d'une espace après le point. Vous devriez utiliser une espace insécable pour cette espace. Cependant, le fait que son insertion [soit assez difficile](https://fr.wikipedia.org/wiki/Espace_ins%C3%A9cable#.C3.80_la_saisie) et que son utilisation n'ait pas encore été testée au sein de Mattermost, pour l'instant il est recommandé d'utiliser des espaces simples.

### Guillemets

Utilisez simplement les guillemets anglophones (`"hello world"`) pour l'instant. Ici aussi, insérer des guillemets francophones dans un formulaire HTML est assez compliqué et leur utilisation n'a pas non plus été testée dans l'interface de Mattermost.

### Pluriel de majesté (We couldn't...)

Il s'avère quelques fois que les messages de Mattermost s'expriment en `nous` plutôt qu'en `il`, par exemple: `We couldn't check the permissions`. Une traduction telle que `Nous ne pouvons pas vérifier les permissions` est tout à fait incorrecte.

De façon à se calquer au plus près des autres traductions, pareil texte sera traduit par `Impossible de vérifier les permissions` plutôt que `Les permissions n'ont pas pu être vérifiées`.

### Traduction trop longue

Si votre traduction s'avère être trop longue pour l'espace octroyé par l'interface utilisateur et si, compte tenu du sens, vous n'êtes pas en mesure d'abbréger la traduction francophone, veuillez exposer le problème sur le [canal "Localization" de Mattermost](https://pre-release.mattermost.com/core/channels/localization).

### Gestion du pluriel

Au sein de Mattermsot, les règles de pluralisation en fonction de la langue sont gérées par la bibliothèque formatjs. Il se peut que vous rencontriez la syntaxe de cette bibliothèque au gré de vos traductions. La syntaxe de formatjs se matérialise comme tel:

    {key, plural, matches}

* `key`: il s'agit de la variable qui représente le nombre d'éléments
* `plural`: il s'agit d'un mot clé fixe (en l'occurrence `plural`) qui indique que le mapping concerne un appel à la bibliothèque formatjs.
* `matches`: il s'agit de la syntaxe propre à formatjs qui va s'occuper de déterminer si la proposition va concerner le singulier, ou le pluriel, voire un nombre particulier (0, 1, 2, etc.).

En place de `matches` peuvent donc se trouver un ou plusieurs des mots clés suivants:

* `zero`: Cette catégorie est utilisée pour les langues qui ont une grammaire spécifique lorsqu'il n'y a aucun élément, comme l'arabe ou le letton. Le français n'étant pas directement concerné par cet élément, on pourra utiliser celui relatif au singulier en lieu et place de cette catégorie.
* `one`: Cette catégorie est utilisée pour les langues qui ont une grammaire spécifique pour un seul élément, ce qui concerne de nombreuses langues. De nombreuses langues asiatiques, comme le chinois ou le japonais, n'utilisent PAS cette catégorie. Le français est conserné par cette grammaire. On utilisera donc ce mot clé, souvent en combinaison de `other`, cf. plus bas.
* `two`: Cette catégorie est utilisée pour les langues qui ont une grammaire spécifique pour deux éléments, comme l'arabe ou le gallois. Le français est également concerné, bien que `other` puisse être utilisé en lieu et place.
* `few`: Cette catégorie est utilisée pour les langues qui ont une grammaire spécifique pour quelques éléments. Certaines langues ont des règles pour 2-4 éléments, d'autres pour 3-10, et d'autres disposent de règles encore plus complexes. Le français n'est pas concerné par cette règle.
* `many`: Cette catégorie est utilisée pour les langues qui ont une grammaire spécifique pour beaucoup d'éléments comme l'arabe, le polonais ou le russe.
* `other`: Cette catégorie est utilisée si aucune value ne correspond à l'une des catégories précédentes. Cette catégorie est souvent utilisée comme la forme pluriel pour certaines langues comme le français ou l'anglais qui ont une grammaire distincte seulement pour les éléments singuliers et ceux pluriel.
* `=value`: Cette catégorie est utilisée pour faire correspondre à une certaine valeur peu importe la catégorie de pluriel utilisée plus haut.

Pour illustrer le [fonctionnement de cette bibliothèque](https://formatjs.io/guides/message-syntax/#plural-format), prenons les exemples suivants.

    New {count, plural, one {message} other {messages}}

donne au sein de l'interface `New message` au singulier et `New messages` pour le pluriel.

En français, 2 versions de traduction sont nécessaires également. Une pour le singulier (`Nouveau message`) et l'autre pour le pluriel (`Nouveaux messages`).

Dans le syntaxe de formatjs, ceci donne la déclaration suivante:

    {count, plural, one {Nouveau message} other {Nouveaux messages}}

Un autre exemple:

    {count, number} {count, plural, one {user} other {users}} of {total, number} total

    {count, number} {count, plural, one {utilisateur} other {utilisateurs}} d'un total de {total, number}

Produira les 2 traductions suivantes: `1 utilisateur d'un total de x` vs `x membres d'un total de x`.

Un autre exemple:

    {count, number} {count, plural, one {Feature} other {Features}} Enabled

    {count, number} {count, plural, one {fonctionnalité activée} other {fonctionnalités activées}}

Comme vous pouvez le voir, selon le contexte, il est possible que vous deviez placer plus de mots dans les accolades de façon à accorder l'ajectif. L'adjectif est en effet invariable en anglais, les chaines anglaises ne tiennent pas compte de ce détail. `1 fonctionnalité activée` vs `x fonctionnalités activées`.

Un autre exemple:

    Every {count, plural, one {minute} other {{count, number} minutes}}

    {count, plural, one {Chaque minute} other {Toutes les {count, number} minutes}}

Ici, il est question d'un changement important, la tournure de phrase ne se traduit pas du tout de la même façon suivant qu'il s'agisse du singulier ou du pluriel: `Chaque minute` vs `Toutes les x minutes`.

## Outils pour le traducteur

[La communauté francophone de KDE](https://fr.l10n.kde.org/pology.php) utilise un outil écrit en python appelé "pology". Cet outil permet d'effectuer toutes sortes d'opérations sur des fichiers po (gettext). Pour en savoir davantage sur les fonctinnalités de pology, [veuillez lire sa documentation](http://pology.nedohodnik.net//doc/user/en_US/index-mono.html).

Installez le paquet correspondant à pology sous votre distribution (sous Arch Linux, utilisez [pology-svn](https://aur.archlinux.org/packages/pology-svn/)) ou clonez le dépôt SVN:

    svn co svn://anonsvn.kde.org/home/kde/trunk/l10n-support/pology

Pour vous assurer que votre traduction dispose d'espaces insécables, ce qui est vivement recommandé en français, téléchargez les fichiers .po de l'instance pootle et exécutez pology de faon à ajouter automatiquement des espaces insécables sur le fichier .po (! le fichier sera modifié, pensez à faire une sauvegarde avant):

    /usr/share/pology/scripts/posieve.py fr:setUbsp ./web_static.po

Les autres commandes de pology telles que `check_rules`, `check_spell`, `check_grammar` et `find_messages` n'ont soit pas été testées, soit ne sont pas compatibles à cause du fait que les chaînes de Mattermost disposent d'une syntaxe particulière propres à la façon dont le langage Go souhaite que les variables soient affichées. La présence de `{{.varName}}`, par exemple, est considérée comme une erreur par pology.

## Vocabulaire

### Attach

| EN | FR |
| --- | --- |
| Error attaching files to post. postId=%v, fileIds=%v, message=%v | Une erreur s'est produite lors du lien des fichiers au message. postId=%v, fileIds=%v, message=%v |
| Unable to attach emoji data to request | Impossible de lier une émoticône à la requête |
| Attaching Files | Joindre des fichiers |
| To import posts with attached files, see {slackAdvancedExporterLink} for details. | Pour importer des messages avec fichiers joints, voir {slackAdvancedExporterLink} pour plus de détails. |

En parlant de pièces jointes (`attachments`) et donc de fichiers, utilisez le terme `joint`/`joindre`.

Dans le cas contraire, utilisez le plus possible la mention de `lien`. En effet, nous utilisons déjà le terme `joindre`/`rejoindre` dans le cas d'un utilisateur joignant/quittant un canal.

### Batch

| EN | FR |
| --- | --- |
| Email batching job's receiving channel was full. Please increase the EmailBatchingBufferSize. | Le canal recevant les e-mail envoyés par lot est plein. Veuillez augmenter le paramètre EmailBatchingBufferSize. |

L'envoi par lots.

### BG

| EN | FR |
| --- | --- |
| Button BG | Arrière-plan du bouton |

`BG` correspond à `background`. On n'utilise pas `fond` mais bien `arrière-plan`.

### Direct

| EN | FR |
| --- | --- |
| Invalid user ID for direct channel creation | ID utilisateur invalide pour la création du canal de messages privés |
| Failed to create direct channel | Impossible de créer le canal de messages privés |
| Failed to create group channel | Impossible de créer le canal de messages de groupe |
| Missing required direct channel property: members | La propriété requise pour un canal de messages privés est manquante: members |

### Enter / specify / input field

| EN | FR |
| --- | --- |
| Please enter your email | Veuillez **spécifier** votre adresse e-mail |
| Please enter an email address | Veuillez **spécifier** une adresse e-mail |
| SHIFT+DOWN (in input field): Highlight text to the next line\n | MAJ+BAS (dans le champ de saisie) : Sélectionne le texte jusqu'à la ligne suivante\n |
| Delete a message by clicking the **[...]** icon next to any message text that you’ve composed | Supprimez un message en cliquant sur l'icône **[...]** située à côté de chaque message que vous avez composé | 

Par mesure de cohérence, la règle générale est d'utiliser le terme `spécifier`. `saisir` est uniquement employé pour qualifier la `zone de saisie`.

Pour ce qui est des messages qui ne spécifient pas une option : une publication, un message de texte, on utilisera le terme `composer`.

### Email

| EN | FR |
| --- | --- |
| Unable to find status of recipient for batched email notification | Impossible de trouver le statut du destinataire pour l'envoi par lot des notifications par e-mail |

Utilisez `adresse e-mail` et non `adresse électronique`. `Adresse électronique` n'a jamais vraiment été utilisé en dehors de la France et tend à être rendu nébuleux à cause des protocoles récents tels que le Bitcoin ou la Blockchain qui, eux, utilisent une adresse que l'on qualifie d'électronique.

### Emoji

On privilégie `émoticône` dans la traduction de Mattermost.

### Endpoint

[cf. section relatives aux APIs et aux routes d'API](#Routes)

### FileInfos

A l'instar de [`NotifyProps`, cf. plus bas](#Notifications push / mobile / desktop), il s'agit du nom d'un objet et doit être traduit en fonction du contexte. Si le message est lié à l'API par exemple, on laissera le terme FileInfos; dans le cas où le message est destiné à l'utilisateur final, on traduira par `informations du fichiers`.

### Flag

| EN | FR |
| --- | --- |
| Flagged Posts | Publications marquées d'un indicateur |
| Flag | Marquer avec un indicateur |
| Flag | Ajouter un indicateur |
| Flag | Marquer |
| Unflag | Supprimer l'indicateur |

Remarquons que plusieurs traductions pour `flag` ont été utilisées ci-dessus. Choisissez simplement celle qui convient en fonction de la taille disponible.

### Follow up

| EN | FR |
| --- | --- |
| Follow up flag | Indicateur de suivi |

Il s'agit simplement des indicateurs pour suivre un message. 

### Get

| EN | FR |
| --- | --- |
| We couldn't get the team members | Impossible de récupérer les membres de l'équipe |

On utilise le terme `récupérer` de façon à assurer une certaine cohérence.

### Hours / timezone

| EN | FR |
| --- | --- |
| {{.SenderName}} - {{.Hour}}:{{.Minute}} {{.TimeZone}}, {{.Month}} {{.Day}} | {{.SenderName}} - {{.Day}}/{{.Month}}, {{.Hour}}:{{.Minute}} {{.Timezone}} |

Le travail de traduction n'implique pas seulement une traduction bête et méchante des chaînes de caractères. Ces dernières doivent également être adaptée en fonction de la coutume ou des habitudes. Dans la francophonie, l'ordre des éléments d'une date n'est pas le même qu'en anglais. Il s'agit là tout d'un travail de localisation.

Ici, en l'occurrence, on placera la date avant l'heure et les éléments de la chaîne de la data seront séparés par un slash (`/`).

### Jobs

| EN | FR |
| --- | --- |
| No indexing jobs queued. | Aucune tâche d'indexation mise en file d'attente. |

Il s'agit du terme `tâche` à employer dans le jargon (cf. les `tâches planifiées` sous Windows).

### Notifications push / mobile / desktop

| EN | FR |
| --- | --- |
| Desktop notifications | Notifications de bureau |
| Invalid Channel Trigger Notify Prop for user. | La propriété utilisateur de déclencheur de notification de canal est invalide. |
| Invalid Comment Trigger Notify Prop for user. | La propriété utilisateur de déclencheur de notification de commentaire est invalide. |
| Mobile Push | Notifications push sur mobile |
| Encountered error when getting files for notification message, post_id=%v, err=%v | Une erreur s'est produite lors de la récupération des fichiers pour la notification de nouvelle publication, post_id=%v, err=%v |
| Invalid Email Notify Prop value for user. | La valeur de la propriété de notification par e-mail est invalide pour l'utilisateur. |

Traduisez les termes `desktop` et `mobile`. N'employez pas le terme `sur le bureau` ou `sur le mobile`.

Faites que votre traduction soit claire lorsqu'il est question de `push`, mentionnez la mantion `notification` lorsqu'elle est absente et n'utilisez par le terme `poussée`. Gardez à l'esprit que notification push tend à être de plus en plus utilisé. Un terme moins employé rendra l'application plus difficile à appréhender.

Veillez à placer la mention `notification` en premier lieu, de façon à rester cohérent avec les termes tels que `notifications push` et `notifications mobiles`. Il s'agit donc bien d'une `notification par e-mail` et non d'un `e-mail de notification`.

Considérez les termes `NotifyProps` et `Notify Props` comme semblables. Ils doivent être traduits. `notify_props` est un champ JSON, conservez le tel quel.

### Permissions

| EN | FR |
| --- | --- |
| You do not have the appropriate permissions | Vous n'avez pas les permissions requises |
| Invalid permissions to regenerate the OAuth2 App Secret | Permissions insuffisantes pour regénérer la clé secrète de l'application OAuth2 |
| Inappropriate channel permissions | Permissions insuffisantes pour ce canal |

Bien que `permissions` et `droits` pourraient tous deux convenir, il a été choisi de privilégier `permissions`. `Permissions invalides` est également à proscrire. Dans le cas du contexte de permissions qui nous concernne, il est en effet question de permissions qui sont trop restrictives et non de permissions d'accès invalides (ex.: permissions UNIX 775 au lieu de 770 par exemple)

### Posted / posts / publication

| EN | FR |
| --- | --- |
| Unable to create /echo post, err=%v | Impossible de créer le message avec la commande /echo, err=%v |
| We couldn't find the pinned posts | Impossible de récupérer les messages épinglés |
| Failed to post update channel header message | Impossible de publier le message indiquant le changement de l'entête du canal |
| Go to Post | Aller au message |

Un `post` ou `poste` est un anglicisme. La règle générale est de garer la mention `message` et le verbe `envoyer` plutôt que `publier`.

Dans de très rares cas, comme lorsqu'on parle d'un fil de discusion, on parlera de `publication`.

Notez que pour `Go to Post`, étant donné que ce texte concerne tous types de messages, il n'est pas visible uniquement pour les publications, mais pour tous les messages. Faites donc attention et veuillez à vous documenter lorsque vous tentez de traduire des parties du logiciel faisant appel à des fonctionnalités que vous ne maîtrisez pas totalement.

Lorsqu'un message est publié par un utilisateur, on dit qu'il est `envoyé`, lorsque le message est publié par le système (message `join`/`leave`/changement d'entête), on dit qu'il est `publié`.

Concernant les messages épinglés, bien que `find` aurait pu être traduit par `trouver`, de façon à assurer une certaine cohérence avec les autres messages d'erreur de ce type, nous employons ici le verbe `récupérer` (cf. [Get](#Get) plus haut).

### Private message

On utilise ici la traduction `Message privé` et non `Message direct` (cf. l'utilisation de `Direct` plus haut).

### Purpose

`Purpose` est souvent employé pour le message de description du canal `purpose message of the channel` par exemple. Il convient donc de le traduire comme `description` dans ce contexte.

### Rate limits

| EN | FR |
| --- | --- |
| Invalid memory store size for rate limit settings. Must be a positive number | Taille du stockage mémoire invalide pour les paramètres de limite de fréquence. Doit être un entier positif. |
| Unable to initialize rate limiting. | Impossible d'initialiser le taux de limite d'appel sur l'API. |

Souvent employé pour désigner une limite de taux. Dans le contexte de Mattermost, il s'agit d'un taux pour limiter le nombre d'appels sur l'API Mattermost que l'utilisateur peut faire dans un temps donné par exemple.

Bien que rencontré parfois dans les domaines du réseau, ce concept de limite n'est pas facile à exprimer en français. Si vous disposez d'une traduction plus appropriée, merci de nous en faire part.

### Routes

| EN | FR |
| --- | --- |
| Initializing team API routes | Initialisation des routes de l'API équipe |
| Auth Endpoint: | Noeud d'authentification (auth endpoint) |

Bien que ces messages devraient être principalement être vus par du personnel technique et donc sachant parler anglais, il est toutefois préférable de les traduire.

Il faut voir une API comme un arbre ou chaque branche est appelée `route` et chaque embranchement (y compris le tout dernier placé en feuille) est appelé un `noeud`. Dans le cas d'une feuille, on appelle souvent ce noeud particulier le `noeud de terminaison` (`endpoint` en anglais). Ici, à cause de l'espace restreint, nous supprimons le terme `de terminaison`. Il est parfois utile de repréciser le terme anglais original; les guides et tutoriels en ligne sont souvent en anglais, avoir le terme en anglais, facilite la correspondance.

Microsoft, dans le cadre de sa plateforme .NET, possède une des rares documentations techniques traduites intégralement en français. Un [article en anglais sur le sujet qui nous préoccupe](https://msdn.microsoft.com/en-us//library/cc668201(v=vs.100).aspx) dispose d'[une correspondance française](https://msdn.microsoft.com/en-us//library/cc668201(v=vs.100).aspx).

On utilise le terme `routage` uniquement dans ce cas-ci :

| EN | FR |
| --- | --- |
| ASP.NET Routing | Routage ASP.NET |

Pour tout le reste, Microsoft utilise au choix : `route` ou `itinéraire`. Dans le cas de Mattermost, de façon à uniformiser les traductions mais également de se rapprocher de la version anglophone, nous utiliserons le terme `route`.

De même, toujours basé sur l'exemple `Initializing team API routes`, nous n'utilisons pas de pluriel pour qualifier le noeud, ni nous n'utilisons de prépositions de lien.

Les propositions suivantes seront donc considérées comme invalides et seront refusées dans Mattermost:

> Initialisation des routes de l'API d'équipe

> Initialisation des routes de l'API des équipes

> Initialisation des routes des APIs d'équipes

> Initialisation des routes des APIs de l'équipe

### Slash commands

Il s'agit des commandes que vous spécifiez lorsque vous commencez votre message par un slash dans Mattermost. La décision a été de traduire ce terme par `commandes slash`.

### SSO

| EN | FR |
| --- | --- |
| SSO / Single Sign-On | Authentification unique (SSO) |

Dans le jargon technique, le terme SSO tend à prendre le pas sur le terme "Authentification unique". Dans le cadre de Mattermost, il a donc été choisi de suffixer la traduction française par le terme SSO entre parenthèses de façon à préciser le contexte. En effet, le terme authentification pourrait être confondu avec le terme authentification multi-facteurs (MFA), autre fonctionnalité présente au sein de Mattermost.

Les traductions telles que "authentification simplifiée" ou "connexion unique" sont à proscrire.

### Token / secret key

* `token`: Utilisez le mot `jeton` à la place.
* `secret key`: `clé secrète` si c'est une clé utilisée dans le sens clé à ne pas divulguer, `clé privée` dans le cas où il est fait mention de clé publique ou s'il est question de chiffrement asymétrique.

### Trigger

| EN | FR |
| --- | --- |
| A trigger word cannot begin with a / | Un mot**-clé** déclencheur ne peut commencer par un / |
