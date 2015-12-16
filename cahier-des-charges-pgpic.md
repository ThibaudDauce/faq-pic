Cahier des charges pour PGPic2
------------------------------

## Objectif du logiciel

Le logiciel a pour objectif d'aider les équipes PIC (Projet INSA Certifiés) de l'INSA de Rouen à mener à bien la gestion de projet ainsi que le suivi de la qualité.

Ce logiciel doit pouvoir être développé de manière itérative. Une grande attention sera donc portée sur la qualité du partage des sources, des tests, ainsi que des procédures de mise à jour et de déploiement du logiciel.

## Fonctionnalités

Comme dit précédemment, les premières fonctionnalités évoquées seront des méta-fonctionnalités du logiciel permettant des mises à jour et des ajouts de fonctionnalités aisément.

### Gestion du projet

#### Gestion des sources

Le logiciel a pour vocation d'être mis à jour par une majorité des personnes. Il est donc nécessaire de prévoir une gestion des sources performante. Le logiciel sera open-source sous license AGPLv3. Il devra être hébergé sur une plateforme de partage de source en ligne utilisant Git. Concernant ces plateformes et compte tenu des différentes fonctionnalités offertes, une liste de solutions gratuites est proposée par ordre de préférence :

* Projet public sur une solution open-source Gitlab CE hébergée en interne à l'INSA
* Projet public sur une solution non libre Github hébergée en ligne
* Projet public sur une solution open-source Gitlab EE hébergée en ligne
* Projet privé sur une solution open-source Gitlab EE hébergée en ligne
* Projet privé sur une solution open-source Gitlab CE hébergée en interne à l'INSA
* Projet privé sur une solution open-source MonProjet hébergé en interne à l'INSA
* Autre solution

Les quatre dernières solutions sont fortement découragées, car la participation au développement du logiciel s'en trouverait fortement impacté.

#### Choix du language et du framework de développement

Le choix du langage est libre, mais il est fortement recommandé d'utiliser un langage maîtrisé par les étudiants ainsi que par une forte communauté, toujours dans l'objectif de favoriser les contributions au projet. Deux langages sont conseillés par ordre de préférence : PHP ou Java.

L'utilisation d'un framework de développement est obligatoire. Le choix du framework de développement est libre mais il est fortement recommandé d'utiliser un framework possédant une forte communauté et de nombreux outils facilitant le développement. Pour le PHP, les frameworks Symfony ou Laravel sont recommandés. Pour le Java, les frameworks **???** ou **???** sont recommandés.

Le développement dans le langage se fera dans le respect des bonnes pratiques concernant les *Coding Styles*.

#### Tests

Une très bonne couverture de test est nécessaire, aucun pourcentage précis n'est requis. Toutes les fonctionnalités doivent être testées au maximum. Chaque résolution de bug doit présenter un test mettant en évidence le problème avant la résolution afin d'éviter toute régression. Les tests unitaires doivent correspondre aux bonnes pratiques de développement et doivent donc être exécutables de manière indépendante et rapide. Ces tests seront exécutés via un système de *Continuous Integration*, une liste de systèmes de *Continuous Integration* est proposée ci-dessous :

* solution open-source Jenkins
* solution open-source Gitlab CI (gestion des sources Gitlab uniquement)
* solution propriétaire Travis CI

Les conventions de développement seront également vérifiées de manière automatique via le système de *Continuous Integration*.

#### Déploiement

Le logiciel doit pouvoir être déployé de manière continue après le passage des tests d'intégration. Ce déploiement doit être un système majoritairement automatisé réduisant au maximum les actions manuelles. Il doit être possible de déployer sereinement plusieurs fois par jour une nouvelle version du logiciel afin de bénéficier de nouvelles fonctionnalités le plus rapidement possible et de limiter les mises en production massives et compliquées.

#### Documentation

Aucune documentation externe n'est exigée, il est toujours préférable de rapprocher la documentation un maximum du code source. Les parties de logique métier difficile à comprendre seront documentés via des commentaires. Toutes les fonctions et toutes les classes seront documentées via des *Doc block*.

La documentation sera générée automatiquement à partir des *Doc block* et sera accessible en ligne. Au fur et à mesure de l'évolution du projet, il sera possible d'ajouter une documentation externe expliquant via des textes simples la logique du logiciel ainsi que son guide utilisation. Nous sommes conscients des difficultés inhérentes à la mise à jour d'une documentation externe, les personnes en charge de vérifier les contributions devront être particulièrement vigilants sur ce point.

#### Contributions

Un guide au format Markdown doit informer les contributeurs de l'objectif du logiciel ainsi que des règles de développement. Toute contribution doit utiliser le système de *Pull Request*. Ces systèmes seront limité à une fonctionnalité par *Pull Request*. Cette fonctionnalité devra comporter des tests et de la documentation. La *Pull Request* devra impérativement passer les tests précédents pour être accepté dans le projet. Un comité d'anciens élèves ASI et de professeurs sera habilité à accepter les *Pull Request* et à fusionner les modifications dans le code de production. La personne en charge de la *Pull Request* devra vérifier notamment la logique métier, la justesse des tests ainsi que la documentation. En fonction du gestionnaire de source choisi (fonctionnalité présente ou pas), une double vérification pourra être obligatoire. Il est conseillé d'utiliser le système de ticket du gestionnaire de source avant toute *Pull Request* afin de discuter de la nouvelle fonctionnalité et des besoins réels. Les étudiants présents en PIC seront les premiers invités à commenter les idées de nouvelles fonctionnalités. Le système de ticket du gestionnaire de source sera également utilisé pour tout bug trouvé dans le code en production, et une *Pull Request* sera également ouverte pour toute correction de bug (comme dit précédemment, un test devra être développé dans la *Pull Request* pour mettre en évidence le bug).

### Fonctionnalités du projet

#### Projet PIC

Il doit être possible de créer des projets et des élèves-ingénieurs en ligne de commande ou via une interface de super-admin. Un projet est composé de :

* un titre (un texte) ;
* un nom de code (un texte) ;
* des élèves-ingénieurs.

Un élève-ingénieur est une partie prenante du PIC. Une partie prenante du PIC est composée de :

* un nom ;
* un prénom ;
* une adresse mail ;

#### Documents

Il doit être possible de créer, de mettre à jour et de supprimer des documents sur le logiciel. Un document possède :

* un type (un *type de document*) ;
* un référentiel (un *référentiel*);
* une référence (un texte);
* un rédacteur (une partie prenante du PIC);
* une date de rédaction (une date);
* un vérificateur (une partie prenante du PIC) ;
* une date de vérification (une date) ;
* un validateur (une partie prenante du PIC) ;
* une date de validation (une date) ;
* un archivage (un booléen).

Si ce document nécessite une approbation, il possède un approbateur (une partie prenante du PIC) et une date d'approbation (une date). Si ce document nécessite une diffusion, il possède une date de diffusion (une date).

Il doit être possible de créer des types de documents avec un nom (un texte), une information sur la nécessité d'approbation (un booléen) et de diffusion (un booléen). Cette ressource doit être extensible pour ajouter des fonctionnalités comme la génération automatique des titres des documents ou un référentiel par défaut.

Il est également possible de créer des référentiels avec un nom (un texte).

La visualisation des documents est effectuée par un tableau récapitulatif avec pour chaque référentiel, les types de documents existants et pour chaque type de document existants la liste des documents présents. Chaque ligne de document présent doit faire figurer, en plus de sa référence, les informations de rédaction, de vérification, de validation, d'archivage et si nécessaire, d'approbation et de diffusion. Ces informations doivent être visuelles pour rapidement déterminer où se trouve le document dans le processus de création. Il doit également être possible d'accéder directement au document dans l'archivage FTP.

#### Temps de travail et tâches

#### Réunions

Le logiciel doit permettre de créer, modifier et supprimer des réunions. Une réunion est composée de :

* un type (un *type de réunion*) ;
* un début (une date et une heure) ;
* une fin (une date et une heure) ;
* une liste de personnes présentes (une liste de *parties prenantes*).

Un type de réunion est un nom (un texte) avec une possibilité de compte-rendu (un *type de document*). Si la réunion est d'un type de réunion nécessitant un compte-rendu, elle doit pouvoir être liée à un document du bon type.

La visualisation des réunions est effectuée par un tableau récapitulatif avec pour chaque semaine et pour chaque date la liste des réunions effectuées. Chaque ligne de réunion doit faire figurer le type de réunion et le temps de la réunion. Si cette réunion nécessite un compte-rendu, il est également nécessaire d'afficher le lien vers l'archivage du compte-rendu ou vers le document dans la liste des documents.

### Cycle correctif
