# ŁØST • HΛWK RAID HELPER

⚔️ *Bot Discord de gestion des raids et des activités de Diablo Immortal.*

ŁØST • HΛWK est un bot Discord conçu pour faciliter l'organisation des clans, la gestion des raids, les événements, les inscriptions des joueurs, les Guerres des Ombres et les rappels automatiques.

Il permet de centraliser les activités de votre serveur Discord et de simplifier la participation des membres grâce à des commandes, des menus interactifs et des messages actualisés automatiquement.

**Aucune installation n'est nécessaire pour utiliser le bot.** Il suffit de l'inviter sur votre serveur Discord.

---

# 🚀 Ajouter le bot à son serveur

## Invitation

👉 **[AJOUTER ŁØST • HΛWK RAID HELPER À MON SERVEUR DISCORD](https://discord.com/oauth2/authorize?client_id=1558792802782019694&permissions=8&integration_type=0&scope=bot)**

Pour ajouter le bot :

1. Cliquez sur le lien d'invitation.
2. Connectez-vous à Discord si nécessaire.
3. Sélectionnez le serveur sur lequel vous souhaitez ajouter le bot.
4. Vérifiez et acceptez les autorisations demandées.
5. Validez l'invitation.

Le bot apparaîtra dans la liste des membres de votre serveur.

*Attention : le lien actuel demande la permission Administrateur. Cela permet au bot de disposer de toutes les permissions du serveur.*

## Après l'invitation

Lorsque le bot rejoint un serveur, il envoie un message de présentation et un guide de configuration dans le salon système du serveur, si celui-ci est disponible.

Un administrateur doit ensuite utiliser `/config` pour définir les différents salons et activer les rappels souhaités.

---

# ⚙️ Configuration du serveur

La configuration est indépendante pour chaque serveur Discord.

Chaque serveur peut utiliser ses propres salons, son propre rôle de notification et ses propres paramètres de rappels.

## La commande `/config`

Cette commande permet de consulter et de modifier les paramètres du bot.

| Paramètre | Fonction |
|---|---|
| `annonces` | Salon des rappels quotidiens de l'Assemblée et de la Chambre forte |
| `gdo` | Salon des rappels de la Guerre des Ombres |
| `logs` | Salon des inscriptions et désinscriptions aux activités |
| `role_ping` | Rôle mentionné dans les raids et les rappels |
| `assemblee` | Activation ou désactivation des rappels quotidiens |
| `guerre_ombres` | Activation ou désactivation des rappels de Guerre des Ombres |

### Exemples de configuration

Définir le salon des annonces :

`/config annonces:#annonces`

Définir le salon de Guerre des Ombres :

`/config gdo:#guerre-des-ombres`

Définir le salon des logs :

`/config logs:#logs-bot`

Définir le rôle à mentionner :

`/config role_ping:@Raid`

Désactiver les rappels quotidiens :

`/config assemblee:False`

Activer les rappels de Guerre des Ombres :

`/config guerre_ombres:True`

Il est également possible de modifier plusieurs paramètres en une seule utilisation de la commande.

### Consulter la configuration

Utilisez simplement :

`/config`

Le bot affiche alors les paramètres actuellement enregistrés pour votre serveur.

**À retenir :**
- Seuls les administrateurs du serveur peuvent utiliser `/config`.
- Vous pouvez modifier un seul paramètre sans toucher aux autres.
- Les paramètres non renseignés conservent leur valeur actuelle.
- La configuration est sauvegardée et conservée après un redémarrage du bot.

---

# 📅 Gestion des raids et des événements

ŁØST • HΛWK dispose désormais de deux types d'activités distincts :

- **Les raids :** événements organisés avec un adversaire, des paramètres de répétition et une gestion avancée.
- **Les événements :** activités classiques créées sans adversaire ni système de répétition.

Les deux systèmes disposent de leurs propres informations et affichages, tout en utilisant un système commun d'inscription des participants.

## Créer un raid

La commande `/raid` permet d'accéder au menu de gestion des raids.

La commande `/gestion_raids` permet également d'accéder au panneau de gestion.

Les raids peuvent notamment comporter les paramètres suivants :

| Paramètre | Description |
|---|---|
| `titre` | Nom du raid |
| `date` | Date et heure au format JJ/MM/AAAA HH:MM |
| `adversaire` | Nom de l'adversaire |
| `description` | Informations complémentaires |
| `places_par_classe` | Nombre maximum de joueurs par classe |
| `repetition` | Fréquence de répétition du raid |
| `jours_avant` | Nombre de jours avant la date prévue pour publier le prochain raid |
| `ping` | Mention à ajouter au message du raid |

La limite de places par classe peut être comprise entre 0 et 100.

Une valeur de `0` signifie qu'il n'y a aucune limite.

## Créer un événement classique

La commande `/event` permet de créer un événement indépendant des raids.

Elle ouvre un formulaire permettant de renseigner les informations de l'activité.

### Paramètres d'un événement

| Paramètre | Description |
|---|---|
| `titre` | Nom de l'événement |
| `date` | Date et heure au format JJ/MM/AAAA HH:MM, facultative |
| `description` | Informations complémentaires |
| `places_par_classe` | Nombre maximum de joueurs par classe |
| `nombre_total_de_places` | Nombre maximum de participants toutes classes confondues |

Une valeur de `0` signifie qu'il n'y a aucune limite pour le paramètre concerné.

La date peut être laissée vide si elle n'est pas encore définie.

**Les événements classiques ne disposent pas de système de répétition.** Chaque événement est créé individuellement.

### Exemple

`/event`

Renseignez les informations demandées dans le formulaire, puis validez.

Le bot publie automatiquement le message d'inscription dans le salon où la commande a été utilisée.

---

# 📝 Inscription des joueurs

Les membres du serveur peuvent participer directement depuis le message de leur raid ou événement.

Chaque message contient les informations de l'activité et la liste des participants inscrits.

### Informations affichées

- Le titre et la description.
- La date et l'heure.
- Le nom du créateur.
- Le nombre total d'inscrits.
- La liste des joueurs répartis par classe.
- Les éventuelles listes d'attente.
- Les statuts de participation.

### Choisir sa classe

Pour s'inscrire :

1. Ouvrez le menu déroulant de l'activité.
2. Sélectionnez votre classe.
3. Renseignez le nom de votre personnage.
4. Validez l'inscription.

Le bot ajoute automatiquement le personnage à la liste de sa classe.

### Classes disponibles

| Classe | Emoji |
|---|---|
| Barbare | 🪓 |
| Chevalier de sang | 🩸 |
| Croisé | 🛡️ |
| Chasseur de démons | 🏹 |
| Druide | 🌿 |
| Moine | 👊 |
| Nécromancien | 💀 |
| Tempête | 🌪️ |
| Sorcier | 🔮 |
| Démoniste | 😈 |

### Liste d'attente

Lorsqu'une limite de places est définie pour une classe, les inscriptions supplémentaires peuvent être placées automatiquement en liste d'attente.

Lorsqu'une place se libère, le premier joueur en attente est automatiquement promu parmi les inscrits.

### Gérer ses inscriptions

Chaque membre dispose de plusieurs possibilités :

- **S'inscrire :** ajouter un personnage dans une classe.
- **Supprimer un personnage :** choisir précisément lequel retirer.
- **Se désinscrire :** retirer ses inscriptions à cette activité.
- **Pas sûr :** indiquer que sa participation est incertaine.
- **Absents :** signaler son absence.

Les modifications sont enregistrées et le message de l'activité est actualisé automatiquement.

---

# 🛠️ Panneau de gestion des raids et événements

La commande `/gestion_raids` permet aux administrateurs d'accéder à une interface interactive de gestion.

L'objectif est de séparer clairement les deux catégories d'activités afin de ne pas mélanger les raids et les événements classiques.

### Organisation du panneau

| Catégorie | Contenu |
|---|---|
| Raids | Liste et gestion des raids |
| Événements | Liste et gestion des événements classiques |

Chaque catégorie permet de retrouver les activités correspondantes et d'accéder à leurs options de gestion.

### Fonctionnalités de gestion

| Action | Description |
|---|---|
| Créer | Ouvre le formulaire de création correspondant |
| Sélectionner | Accède aux informations d'une activité |
| Fermer / rouvrir | Bloque ou autorise les nouvelles inscriptions |
| Participants par classe | Consulte les participants d'une classe |
| Modifier | Modifie les informations d'une activité |
| Supprimer | Supprime une activité après confirmation |
| Actualiser | Recharge la liste des activités |
| Exporter les personnages | Génère un lien d'export vers le site |

Les options de répétition sont réservées aux raids.

### Fermer les inscriptions

Une activité peut être fermée pour empêcher les nouvelles inscriptions.

Elle peut être rouverte à tout moment depuis le panneau de gestion.

### Exporter les participants

Le panneau de gestion permet de générer un lien vers le site associé au bot.

Les personnages inscrits sont exportés avec :
- Leur pseudo.
- Leur classe.
- Leur emoji de classe.

Le site peut ainsi récupérer les personnages à partir du lien généré.

🌐 **Site :** http://lostxhawk.ooguy.com/

---

# 🔁 Répétition des raids

Les raids peuvent être configurés pour se reproduire automatiquement.

Quatre modes sont disponibles :

| Mode | Fonctionnement |
|---|---|
| Aucune | Raid unique |
| Chaque jour | Reproduction quotidienne |
| Chaque semaine | Reproduction hebdomadaire |
| Chaque mois | Reproduction mensuelle |

**Cette fonctionnalité concerne uniquement les raids. Les événements classiques créés avec `/event` ne sont pas répétitifs.**

### Publication automatique

Le paramètre `jours_avant` permet de définir combien de jours avant la prochaine occurrence le bot doit publier le nouveau raid.

Il est possible de choisir une valeur comprise entre 0 et 30 jours.

Par exemple :

- Raid hebdomadaire.
- Publication 1 jour avant.
- Le prochain raid est automatiquement créé la veille de sa date prévue.

Les nouveaux raids possèdent leurs propres inscriptions et leur propre liste de participants.

### Modifier une répétition

Deux possibilités :

- `/raid_repetition` : modifier la répétition d'un raid à partir de son identifiant.
- `/gestion_raids` : modifier la répétition depuis le panneau interactif.

Les paramètres de répétition sont appliqués à l'ensemble de la série concernée.

---

# 📋 Commandes disponibles

Voici les principales commandes du bot.

| Commande | Utilité |
|---|---|
| `/config` | Consulter ou modifier la configuration du serveur |
| `/raid` | Ouvrir le menu de gestion des raids |
| `/event` | Créer un événement classique |
| `/raid_create` | Créer un raid, si cette commande est disponible sur votre version |
| `/raid_list` | Afficher les raids enregistrés |
| `/raid_close` | Fermer ou rouvrir les inscriptions |
| `/raid_delete` | Supprimer un raid |
| `/raid_export` | Afficher les inscrits répartis par classe |
| `/raid_repetition` | Modifier la répétition d'un raid |
| `/gestion_raids` | Ouvrir le panneau interactif de gestion |
| `/placements` | Publier les placements de Guerre des Ombres |
| `/sync` | Synchroniser les commandes Discord |

*Certaines commandes sont réservées aux administrateurs du serveur ou aux super administrateurs du bot.*

---

# ⚔️ Guerre des Ombres

Le bot dispose d'un système de rappels automatiques pour les Guerres des Ombres.

Les rappels sont envoyés dans le salon défini avec le paramètre `gdo` de la commande `/config`.

### Horaires des rappels

Les rappels sont programmés le jeudi et le samedi, selon les horaires suivants :

| Heure | Notification |
|---|---|
| 18 h 30 | Guerre des Ombres dans 1 heure |
| 19 h 15 | Guerre des Ombres dans 15 minutes |
| 19 h 25 | Guerre des Ombres dans 5 minutes |
| 19 h 30 | Début de la Guerre des Ombres |

Le rôle configuré avec `role_ping` peut être mentionné dans les messages.

### Activation et désactivation

Pour activer les rappels :

`/config guerre_ombres:True`

Pour les désactiver :

`/config guerre_ombres:False`

---

# 🏰 Assemblée et Chambre forte

ŁØST • HΛWK propose également des rappels quotidiens pour les activités de l'Assemblée et de la Chambre forte.

Les rappels sont envoyés dans le salon configuré avec le paramètre `annonces`.

### Horaires

| Heure | Activité |
|---|---|
| 12 h 00 | Rappel quotidien |
| 19 h 00 | Rappel quotidien |

Les rappels sont programmés du lundi au samedi.

Le bot publie l'image associée aux activités et peut mentionner le rôle configuré.

### Activation et désactivation

Activer :

`/config assemblee:True`

Désactiver :

`/config assemblee:False`

---

# 🧩 Gestion des placements de Guerre des Ombres

La commande `/placements` permet de publier directement sur Discord les compositions d'équipes préparées depuis le site.

Elle utilise un code de placement au format `HTO1:`.

### Comment publier des placements ?

1. Préparez vos équipes sur le site associé au bot.
2. Générez votre code de placement.
3. Copiez le code complet.
4. Sur Discord, utilisez `/placements`.
5. Collez le code dans le paramètre `code`.
6. Validez la commande.

Le bot décode automatiquement les informations et publie un embed contenant les équipes.

### Informations affichées

- Nom des placements.
- Catégories.
- Numéros des équipes.
- Pseudos des joueurs.
- Emojis associés aux joueurs.
- Nombre total de joueurs placés.

Si le code est incomplet ou invalide, le bot affiche un message d'erreur.

---

# 📨 Système de logs

Le bot peut enregistrer les principales opérations d'inscription dans un salon dédié.

Le salon se configure avec :

`/config logs:#logs-bot`

Les événements enregistrés comprennent notamment :

- Les nouvelles inscriptions.
- Les désinscriptions.
- Les suppressions de personnages.

Les messages de logs indiquent l'utilisateur concerné, le personnage lorsque disponible, la classe et l'activité associée.

Cela permet aux responsables du serveur de suivre l'activité des inscriptions.

---

# 💾 Sauvegarde et conservation des données

Les paramètres et les activités sont enregistrés séparément pour chaque serveur.

Les informations sauvegardées comprennent notamment :

- Les salons configurés.
- Le rôle de notification.
- L'état des rappels.
- Les raids créés.
- Les événements classiques.
- Les inscriptions.
- Les listes d'attente.
- Les paramètres de répétition des raids.

Les données sont conservées lors des redémarrages du bot.

Les messages d'inscription existants sont également réenregistrés au démarrage afin de permettre aux interfaces persistantes de continuer à fonctionner.

---

# ❓ Questions fréquentes

### Faut-il installer quelque chose ?

Non. Il suffit d'inviter le bot sur son serveur Discord. Toutes les fonctionnalités sont accessibles depuis Discord.

### Qui peut configurer le bot ?

Les administrateurs du serveur peuvent utiliser `/config` pour définir les paramètres.

### Quelle est la différence entre `/raid` et `/event` ?

`/raid` concerne les raids avec adversaire et possibilité de répétition.

`/event` permet de créer des événements classiques sans adversaire ni répétition.

### Les membres peuvent-ils s'inscrire eux-mêmes ?

Oui. Ils utilisent les menus et boutons présents sur les messages des raids et événements.

### Peut-on inscrire plusieurs personnages ?

Oui. Un membre peut inscrire plusieurs personnages et les gérer individuellement.

### Que se passe-t-il lorsqu'une classe est complète ?

Les inscriptions supplémentaires peuvent être placées automatiquement en liste d'attente.

### Les événements peuvent-ils être répétitifs ?

Les raids peuvent être répétitifs. Les événements classiques créés avec `/event` sont des activités individuelles.

### Chaque serveur possède-t-il sa propre configuration ?

Oui. Les paramètres, les raids et les événements sont séparés par serveur.

### Le bot fonctionne-t-il après un redémarrage ?

Oui. Les données sont sauvegardées et les interfaces d'inscription persistantes sont réenregistrées au démarrage.

### Comment obtenir de l'aide ?

En cas de problème, contactez l'équipe responsable de ŁØST • HΛWK.

---

# ⚔️ ŁØST • HΛWK

*Une gestion centralisée, des inscriptions simplifiées et une meilleure organisation pour vos activités Diablo Immortal.*

**Site officiel :** http://lostxhawk.ooguy.com/

**Invitation Discord :** [Ajouter ŁØST • HΛWK](https://discord.com/oauth2/authorize?client_id=1558792802782019694&permissions=8&integration_type=0&scope=bot)
