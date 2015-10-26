# Qualité

  - [Outils pratiques](#outils-pratiques)
  - [Cycle correctif](#cycle-correctif)
  - [Rédaction de documents](#redaction-de-documents)
  - [Pour chaque lot](#pour-chaque-lot)
  - [Recette](#recette)
  - [Réunion hebdomadaire](#reunion-hebdomadaire)
  - [Rédaction d'un État des Configurations](#redaction-dun-etat-des-configurations)
  - [Formation et compétences](#formation-et-competences)

## Outils pratiques

  * Script d'archivage des documents en SFTP : [AntoineAugusti/PdfArchiver](https://github.com/AntoineAugusti/PdfArchiver)

## Cycle correctif

#### Quand lever un FT (Fait Technique)

  * Remarque du client ou de Meslier sur un document qu'on lui a soumis pour approbation
  * Dépassement d'un indicateur
  * Modification à effectuer dans un document ayant été approuvé
  * Déclenchement d'un risque

#### Rédiger une FFT (Fiche de Fait Technique)

  * Ajout d'un FT
  * Remplir la partie rédaction
  * Cocher la case rédaction terminée

#### Analyse

  * Créer une CTFT (Commission de Traitement des Faits Techniques) composée d'au moins le chef PIC, le responsable qualité et le responsable gestion des configurations
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

**Penser à faire les PV de début de sprint (PVDS) et fin de sprint (PVFS).**

#### Phase de spécifications

  * Mettre à jour le DSE
  * Approbation client
  * PVDSE
    -
  * Mettre à jour le DSI
    -
  * Mettre à jour le PTV
  * Approbation client
  * PVPTV
    -
  * PVFPS
    -
  * Créer un nouveau CDR vierge correspondant au lot
  * Approbation client

#### Phase de conception

**Tâches en parallèle :**

  * Mettre à jour le DC
  * Mettre à jour le PTI
  * Mettre à jour le PTU

#### Phase de développement

#### Phase de tests

  * Déroulement des tests unitaires prévus dans le PTU
  * Conservation des journaux de résultat
    -
  * Déroulement des tests d'intégration suivant le PTI
  * Conservation des journaux de résultat

#### Phase de validation interne

  * Déroulement des tests prévus dans le PTV = déroulement du CDR du lot
  * Conservation des journaux de résultat
  * PVVV

#### Phase de livraison

  * EC récapitulant les éléments de la livraison
  * PVL
  * [Partie Recette](#recette)

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
  * Passer en revue les risques
  * En cas de modification d'un risque (création, mise à jour ou clôture)
    * Effectuer les changements sur la fiche de risque correspondante (ne pas oublier le tableau de suivi des modifications)
    * Répercuter les changements sur le portefeuille de risques (ne pas oublier le tableau de suivi des modifications)
    * Le pilote du risque doit envoyer un mail montrant qu'il valide les changements du risque

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
