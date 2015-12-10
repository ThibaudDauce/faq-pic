# Introduction

Ce document recense les bonnes pratiques à adopter lors de la gestion d'un PIC et a pour but de décrire les spécificités du déroulement de ce dernier. La première partie traite des bonnes pratiques pour le Suivi de la Qualité. Le seconde aborde la gestion de projet.

# Suivi de la Qualité

Cette partie est constituée d’une énumération des bonnes pratiques à suivre afin d’assurer une bonne veille qualité au sein du PIC.

  - [Outils pratiques](#outils-pratiques)
  - [Cycle correctif](#cycle-correctif)
  - [Rédaction de documents](#redaction-de-documents)
  - [Pour chaque lot](#pour-chaque-lot)
  - [Recette](#recette)
  - [Réunion hebdomadaire](#reunion-hebdomadaire)
  - [Rédaction d'un État des Configurations](#redaction-dun-etat-des-configurations)
  - [Formation et compétences](#formation-et-competences)
  - [Tâches liées au changement de semestre](#taches-liees-au-changement-de-semestre)
  - [Divers](#divers)

## Outils pratiques

  * Script d'archivage des documents en SFTP : [AntoineAugusti/PdfArchiver](https://github.com/AntoineAugusti/PdfArchiver)

## Cycle correctif

#### Quand lever un FT (Fait Technique)

  * Remarque du client ou de Directeur Qualité sur un document qu'on lui a soumis pour approbation
  * Dépassement d'un indicateur
  * Modification à effectuer dans un document ayant été approuvé
  * Déclenchement d'un risque

#### Rédiger une FFT (Fiche de Fait Technique)

  * Ajout d'un FT
  * Remplir la partie rédaction
  * Cocher la case rédaction terminée

#### CTFT

  * Créer la réunion et la CTFT sur PGPic avant le début de cette dernière
  * Rédiger les Comptes-Rendus (ceux-ci n’ont pas besoin d’être validés et diffusés)

#### Analyse

  * Créer une CTFT (Commission de Traitement des Faits Techniques) composée d'au moins le chef PIC, le responsable qualité et le responsable de la gestion des configurations
  * Faire l'analyse des n pourquoi sur la FFT
  * Créer une FOC (Fiche d'Ordre de Correction) avec :
    * Corrections détaillées à faire
    * Vérifications
    * Conditions de clôture (**un FT concernant un document soumis à approbation ne peut pas être clôturé tant que le document n'est pas approuvé de nouveau**)

#### Correction

  * Faire les corrections
  * Cocher la case correction terminée
  * Spécifier la date de correction dans la case "Commentaires sur la vérification"

#### Vérification

  * Vérifier les points de vérifications de l'OC (Ordre de Correction)

#### Clôture

  * Organiser une CTFT
  * Le responsable gestion des configurations doit clôturer la FOC et la FFT

#### Analyse à froid

  * Organiser une CTFT après une durée plus longue (si la FFT ne comporte pas d'action corrective, l'analyse à froid n'est pas utile)

#### Archivage des fiches

  * Avec l'assistant d'impression (ctrl-p), exporter au format PDF (**Attention, la date de vérification des FOC ne s'affiche pas correctement, il faut la changer à la main dans le HTML**)
  * L'archivage des CTFT doit se faire en Latex (voir modèle)

## Rédaction de documents

**Attention : si des modifications sont faites dans le PQ ou le PGC, elles ne peuvent être mises en pratique seulement quand le document a été approuvé par Meslier.**

#### Nouveau document

  * Vérifier son emplacement et son nommage grâce au PGC en vigueur
  * **Document avec version :** V1.00
  * **Document sans version :** mettre "création" en première ligne du suivi des modifications
  * **Document soumis à approbation :** ajouter le tableau des signatures
  * Rédaction du document
  * **Document soumis à approbation :**
    * Vérification
    * Validation
    * Approbation
    * Mise à jour des signatures
  * Diffusion si nécessaire
  * Archivage sur FTP et accès sur PGPic (onglet documents)

#### Mise à jour d'un document existant

  * **Document avec version :** augmenter la version courante
  * **Document sans version :** ajout d'une ligne dans le suivi des modifications avec la nature de la modification (référence à un CR, à une FOC, ou contenu de la modification)
  * **Document soumis à approbation :** utiliser le code couleur pour faciliter la relecture (`\textcolor{ajout}{text}` ou `\color{ajout}long text\color{black}`, vous pouvez utiliser `ajout`, `modif` ou `suppr`)
  * Rédaction du document
  * **Document soumis à approbation :**
    * Vérification
    * Validation
    * Approbation
    * Mise à jour des signatures
  * Diffusion si nécessaire
  * Archivage sur FTP et accès sur PGPic (onglet documents)

## Pour chaque lot

  * revue formelle de démarrage de sprint (RFDS) -> émission PV début sprint (PVDS)
  * réunion client pour définir les objectifs, tâches… (ne pas oublier le compte-rendu)

#### Phase de spécifications
  Les spécifications comportent le Document de Spécifications Externes (DSE), Document de Spécifications Internes (DSI) et le Plan de Tests de Validation (PTV).

  * Mettre à jour le DSE
  * Approbation client du DSE
  * Revue du dossier des spécifications externes (RDSE) -> émission PV de revue de DSE (PVDSE) -> à faire signer et archiver
    -
  * Mettre à jour le DSI
    -
  * Mettre à jour le PTV
  * Approbation client du PTV
  * Revue du plan de tests de validation (RPTV) -> émission PV de revue de PTV (PVPTV) -> à faire signer et archiver
    -
  * Une fois les spécifications terminées, revue formelle de fin de phase de spécifications (RFFPS) -> émission PV de fin de phase de spécification (PVFPS) -> à faire signer et archiver
    -
  * Créer un nouveau Cahier de Recette (CDR) vierge correspondant au lot
  * Approbation client

#### Phase de conception
  La conception comporte le Document de Conception (DC) - composé du Document de Conception Préliminaire (DCP) et du Document de Conception Détaillée (DCD) - du Plan de Tests d'Intégration (PTI), du Plan de Tests Unitaires (PTU). Le PTI est rédigé lors du DCP et le PTU lors du DCD.

  * Mise à jour DCP
  * Mise à jour PTI
  * À la fin de la conception préliminaire, revue de conception préliminaire (RCP) -> émission PV de fin de conception préliminaire (PVFCP) -> à faire signer et archiver
  * Mise à jour DCD
  * Mise à jour PTU
  * À la fin de la conception détaillée, revue de conception détaillée (RCD) -> émission PV de fin de phase de conception (PVFPC)

#### Phase de développement

#### Phase de tests

  * Déroulement des tests unitaires prévus dans le PTU
  * Conservation des journaux de résultat
    -
  * Déroulement des tests d'intégration suivant le PTI
  * Conservation des journaux de résultat

#### Phase de validation interne

  * Déroulement des tests (TU et TI) prévus dans le PTV = déroulement en interne du CDR du lot
  * Conservation des journaux de résultat
  * Revue formelle de fin de phase de validation (RFFPV) -> émission d'un procès verbal de vérification et de validation (PVVV) -> à faire signer et archiver

#### Phase de livraison

  * Faire l'État des Configurations (EC) récapitulant les éléments de la livraison
  * Après la livraison, PV de livraison (PVL) -> à faire signer et archiver
  * [Partie Recette](#recette)
  * Une fois la recette acceptée et approuvée, PV de recette (PVR)
  * À la fin du sprint, revue formelle de fin de sprint (RFFS) -> émission PV de fin de sprint (PVFS)

## Recette

Voir le PTV chapitre 2.

#### Avant la recette

  * Envoyer au client le CDR correspondant au type de recette (provisoire ou définitive), ce CDR est basé sur la version vierge créée au moment de la phase de spécification

#### Durant la recette

  * Effectuer tous les tests décrits dans le cahier de recette (dire si ils sont OK)
  * **En cas de test non validé :** créer une FFT
  * Les résultats doivent être consignés dans le CDR (pas le vierge)

#### Fin de la recette

  * Conclusion: acceptation ou rejet du lot
  * La conclusion doit être inscrite dans le CDR (pas le vierge)

#### Après la recette

  * Approbation par le client du CDR complété

#### Nota-bene

Si par exemple le CDR doit être modifié entre la séance de recette provisoire et celle définitive (ex : pour vérifier plus en profondeur des critères non validés la première fois), c'est le CDR vierge qui change de version. Il doit être de nouveau approuvé par le client. Les CDR provisoires (ou définitifs) changent de version lorsque l'on ajoute les résultats de la séance de recette (annotations du client).

## Réunion hebdomadaire

**Ne pas oublier le CR**

  * Remplir le tableau de bord des indicateurs de la semaine précédente
    * La date du nouveau TB correspond à la date du lundi de la semaine concernée (la précédente)
    * Remplir l'onglet "tableaux"
    * Vérifier que les graphiques (onglet "graphiques") s'affichent correctement (plage de données trop petite ?)
    * En cas de dépassement d'un indicateur, ajouter une ligne dans l'onglet "dépassement" et créer une FFT ([voir cycle correctif](#cycle-correctif))
    * Exporter le TB au format PDF et l'archiver (FTP et PGPic)
    * REMARQUE : Pour changer les valeurs des indicateurs (cible et seuil), il faut modifier le PQ et créer une Fiche de Faits Techniques. Cependant si l’information n’est pas présente dans le PQ, la création d’une Fiche de Faits Techniques n’est pas obligatoire.
  * Passer en revue les risques
  * En cas de modification d'un risque (création, mise à jour ou clôture)
    * Reprendre les causes source et trouver des actions préventives
    * Mettre à jour les risques sur PGPic
    * Effectuer les changements sur la fiche de risque correspondante (ne pas oublier le tableau de suivi des modifications)
    * Répercuter les changements sur le portefeuille de risques (ne pas oublier le tableau de suivi des modifications)
    * Le pilote du risque doit envoyer un mail montrant qu'il valide les changements du risque
    * Vérifier que tous les membres sont pilote d’un risque

## Rédaction d'un État des Configurations

#### Quand

  * Livraison client
  * Inspection technique

#### Documents à livrer

  * Lister les documents demandés dans la livraison **avec leur numéro de version ou de commit**
  * Mettre en parallèle les documents cités en référence
  * Si un document n'est pas encore rédigé, le spécifier afin de montrer que ce n'est pas un oubli

#### Documents en référence

  * Les documents cités en références propres au PIC doivent être transmis en même temps que les documents réellement demandés

#### Références en cascade

  * Tous les documents cités en référence doivent être consignés dans un deuxième tableau reprenant leurs propres références
  * Ainsi de suite jusqu'à ce qu'aucune référence ne soit plus possible

## Formation et compétences

#### Avant toutes les formations (début de semestre)

Rédaction du plan de formation (PF) avec les formations à prévoir et leur date

#### Avant une formation

  * Rédaction de la fiche
    * Contenu
    * Modalités de l'évaluation à chaud
    * Modalités de l'évaluation à froid
    * Date effective
    * Personnes formées
    * …

#### Formation

Déroulement de la formation suivant ce qui était prévu

#### Évaluation à chaud

  * Suivre les modalités prévues
  * Garder une trace écrite (**pas de crayon à papier**) ou numérique des résultats obtenus pour chaque membre formé
  * Mettre à jour la fiche de formation avec les résultats de l'évaluation à chaud

#### Report des compétences obtenues

  * Mise à jour des fiches de compétences des personnes ayant validé la formation (ne pas oublier le tableau de suivi des modifications au début et le tableau des formations à la fin)
  * Les fiches modifiées doivent être validées par mail par leur propriétaire

#### Mise en œuvre

Utilisation des compétences

#### Évaluation à froid

  * Mesure si la mise en œuvre est correcte
  * Résultats consignés dans la fiche de formation
  * Tableaux des formations et fiches de compétences sont mis à jour

## Tâches liées au changement de semestre

* Ajouter les nouveaux membres dans le Plan de Formation
* Créer leur fiche de compétence
* Réattribuer les risques dont les pilotes sont partis
* Mettre à jour le PQ
* Imprimer des nouveaux engagements de confidentialité et les faire signer aux nouveaux membres

## Divers

* Reprendre les notes des questionnaires de satisfaction après les revues
* Scanner et archiver les rapports d’audit et d'inspections technique
* Archiver les anciens comptes-rendus et cocher les cases associées dans PGPic
* Lors de l’envoi pour approbation du PQ et du PGC, envoyer également les
Fiches d’Ordre de Correction correspondantes (à imprimer dans un pdf)


# Gestion de projet

Cette partie est constituée d’une énumération des bonnes pratiques à suivre afin de mener à bien une gestion de projet en accord avec la norme ISO 9001:2008, le cycle en V imposé par les méthodes de rédaction des documents et enfin la méthode SCRUM qui rythme la vie du projet. Il s’agit bien entendu d’une liste exhaustive s’appliquant particulièrement à la gestion de l’équipe PIC tantPic.

  - [Pgpic](#Pgpic)
  - [SCRUM](#scrum)
  - [Mails](#mails)
  - [Réunions](#reunions)
  - [Recettes](#recettes)
  - [Utilisation des tableaux](#utilisation-des-tableaux)

## Pgpic
### Tâches

* Faire attention aux dates de fin de tâche, si une s’arrête le vendredi, on ne pourra pas se cocher dessus ce jour, il faut toujours mettre la date de fin de tâche le lendemain. Par défaut mettre la date de fin de tâche le samedi
* Pour la mise à jour des tâches : regarder celles qui ne sont pas à 100% et dont la date est passée. Agir en conséquence, soit en mettant le pourcentage à jour, soit en prolongeant la tâche
* Ne pas hésiter à rappeler aux membres de l’équipe de mettre à jour les pourcentages des tâches en cours. C’est le seul moyen de visualiser l’avancement de ces dernières
* Penser à sauvegarder le GANTT chaque semaine après qu’il soit mis à jour. Une fois qu’il est sauvegarder il est consultable à chaque sauvegarde effectuée
* Il est inutile d’indiquer la durée des taches car elle n’est pas gérée
* Tenir un planning/rétro-planning simplifié sous un tableur en parallèle
* Bien faire attention à créer les tâches le Vendredi ou le week-end pour la semaine à venir. Cela permet à chaque membre de commencer la semaine en sachant ce qu’il a à faire
* Il ne faut pas hésiter à consulter l’onglet tâche de PgPic pour superviser les tâches disponibles pour l’ensemble des membres
 
### Réunions

* Toujours créer les réunions avant de les lancer
* Essayer de toujours arrêter la réunion depuis l’onglet où elle a été lancé pour ne pas décocher tout le monde à la fin de la réunion
* Créer les réunions dans PGPic dès que les dates sont disponibles
 
## SCRUM

1. Liste des scénarios (Possible de les mettre sous forme de fonctions)
2. Planning poker avec les membres de l’équipe
3. Redécomposer les "user-stories" sur les post-it du scrumboard avec les différentes phases du cycle en V (Spécification-Conception-Développement-
Tests)
4. Préparer le Burndown Chart
5. Préparation du scrumboard (Afficher le backlog de chaque scénario à côté pour voir les détails de chaque tâche)
6. Bien garder les post-it concernant les documents du PIC et les différentes actions (Installations logiciels, ...). Garder un code couleur pour plus de clarté

Les étapes 1 à 3 sont préparables avant le début du sprint suivant ce qui permet d’enchaîner les sprint beaucoup plus facilement

* Bien faire les Daily-Scrum
* Effectuer les rétrospective de sprint, afin de toujours améliorer les méthodes de travail de l’équipe

## Mails

* Faire des dossiers pour archiver les mails créer un dossier par personne pour plus de clarté et d’organisation
* Archiver les mails à chaque fin de sprint
* Une fois les mails archivés, reprendre une architecture vierge
* Annoncer les ordres du jour des réunions pédagogiques et hebdomadaires

## Réunions

* Ne pas oublier le suivi des risques lors des réunions hebdomadaires 

## Recettes

* Cahier de recette : se baser sur ceux déjà faits, rédigeable à 90% une fois les spécifications faites
* Envoyer le cahier de recette idéalement 1 semaine avant la livraison au client
* Quand le développement est bien avancé, dérouler le cahier de recette en interne pour voir les potentiels bugs et problèmes à corriger
* Ne jamais préparer le livrable le jour même car cela demande beaucoup de temps
* Lister précisément les points restants pour boucler le livrable
* Diffuser l’archive du livrable en interne et le tester sur plusieurs machines pour vérifier que les chemins des dépendances ne sont pas en absolu

## Utilisation des tableaux

* Beaucoup utiliser les tableaux, le visuel est plus efficace pour que tout le monde suive bien les points importants 

