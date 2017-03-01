---
layout: post
title: 1er mars - notes de travail
date: '2017-03-01 13:40'
tags: 'corpus, TEI, indexation,'
---

<!-- category: méthodologie -->

> Le Général Instin bouge encore. Notre session de travail coïncide avec sa toute dernière publication sur Remue.net : [Nig le chien [1 & 2]](http://remue.net/spip.php?article8721) dans la récente rubrique [Spoon River](http://remue.net/spip.php?rubrique997).

Un mois que l'on s'emploie à collecter notre corpus Instin. Ne sachant pas encore trop dans quelle direction le tirer, nous l'avons initié avec un corpus test en aspirant une dizaine d'articles de Remue.net. Pour chacun de ces articles, nous avons maintenu un inventaire en l'enrichissant d'un certain nombre de métadonnées.

Les métadonnées s'organisent pour le moment ainsi :

Pour chaque entrée :

` * **Objet** : recense les données propres au document ou à l'objet collecté
    * titre
    * auteur(s) identifié-e(s)
    * url ressource (qui identifie l'objet sur le web)
    * url référence (en cas d'objet orphelin ou "déporté", le lien qui nous a guidé vers l'objet)
    * date de création (dans le cas où la rédaction/production de l'objet/évenement est spécifié)
    * date de publication (dans le cas où la ressource/objet a une date de publication)
  * **Indexation** : décrit l'objet selon notre propre taxonomie (en construction)
    * mots-clés
    * description
    * corpus : Instin, documentation,
    * date d'archive
    * genre: écrit, article, poème, haiku,
    * matérialité : print, numérique, wall, performance, conférence
    * liens à d'autres entrées
    * propagation
`

A titre d'exemple :

` * item-016
	 * **Objet**
	    * titre: l’Électroencéphallusgramme
	    * auteur: Delphine Bretesché
  	  * url ressource: http://remue.net/spip.php?article3108
	    * geolocalisation:
      * url référence:
      * date de création:
	    * date de publication: 2009-03-03
	 * **Indexation**
		 * corpus : primaire. Rubrique rubrique RemueNet/dossiers/écrivains/Général Instin/les noms/
     * description: Performance Électroencéphallusgramme du Général Instin, encre, bâton, rotring et scotch sur rouleau de papier. Contient du matériel visuel + un texte
     * mots-clés:
		 * date d'archive: 2017-02-12 (servanne)
		 * genre:
		 * matérialité: numérique
		 * site d'origine: remue.net
	   * liens:
		      * http://remue.net/spip.php?article2813 [item-021]
		      * http://delphinebretesche.hautetfort.com **étrange ce truc**
		      * http://remue.net/spip.php?article2843#phase [item-020]
		      * http://remue.net/spip.php?article1502#charte [item-019]
		      * http://remue.net/spip.php?article2156#spasme [item-017]
		 * propagation:
`
Pour ce corpus test d'une dizaine d'entrées, la collecte s'est fait par propagation hypertextuelle. A partir d'un premier article, nous avons simplement identifié les liens auxquels l'article fait référence (Remue.net présente un maillage interne particulièrement dense), et nous avons considéré ces nouveaux liens (interne à Remue.net) comme les prochaines entrées de notre corpus test. Nous aurions pu prendre une méthode d'échantillonage plus classique : par date, par auteur, par rubrique, mais cet échantillonage a le mérite d'explorer la base de Remue.net de manière relativement aléatoire, bien que par définition dans un sens anté-chronologique.

Très rapidement, ce corpus test s'est enrichi d'une trentaine d'entrées.

## Maîtriser le corpus

Dans l'objectif de procéder à plusieurs traitements sur ce corpus, notamment cartographie et textométrie, nous passons maintenant l'archive HTML dans une version XML TEI. Cet effort de caractérisation plus précise du corpus nous ouvre de nouvelles pistes de réflexion pour le projet.

C'est en quelque sorte une première étape d'éditorialisation d'une archive et ce processus d'éditorialisation nous projette dans une double dynamique :

* dynamique d'ouverture : dans la continuité de l'esprit du Général Instin, cette éditorialisation pourrait avoir vocation à devenir publique, accessible, appropriable.
* dynamique réflexive sur notre projet : en faisant le pari que la conception du dispositif d'éditorialisation de l'archive nous éclairera sur le dispositif GI lui-même.

Ce pari est celui d'un dialogue entre le dispositif de publication littéraire du GI et le dispositif d'une archive scientifique. Un dialogue tout en tension, tout en contradiction peut-être, mais dont la démarche fait sens pour considérer l'archive non pas comme une tentative de totalisation de GI, mais plutôt de projection en miroir, elle-même excroissance du projet.

## Dézoom

Notre corpus comprend maintenant une trentaine d'entrées. Ce premier test nous a permis de réfléchir à une structuration encore en mouvement de notre corpus. Première étape utile et rassurante, mais qui nous laisse tout à fait démunis (voir angoissés) au regard de l'ampleur de la tâche.

Pour entrer sereinement dans la deuxième étape de collecte, celle de l'exhaustivité (!), il nous faut dézoomer, prendre un peu de hauteur et examiner la structure générale du Général. Tentative de chronologie, cartographie des plateformes, arborescence des plateformes.

### Ébauche par date

* 1997
  * «GI projet interdisciplinaire et collectif»
  * soirée de performances au squat de la Grange-aux-Belles (Paris)
* 1998
  * performance Mômô Basta (défiguré)
* 2005 : repris dans la revue papier d'art et littérature _Éponymes_ (2005-2007)
* 2007 : Démarrage du feuilleton sur Remue.net avec plusieurs rubriques :

### Remue.net : arborescence de la rubrique "Général Instin"

  * **traits**
    * _"aperçus du projet, pensées, aphorismes, essais critiques"_
    * publications de mars 2006 à juin 2016
  * **noms**
    * _"grandes figures du projet"_
    * publications de mars 2009 à mars 2016
  * **réels**
    * _"récits d'évenements autour du projet"_
    * publications de mars 2006 à 8 mars 2016
    * 19 contributions
  * **générales**
    * _"formes diverses d'Instin, fictions, traces, fusées,..."_
    * 2006 à 2016
  * **portrait géomantique du GI**
    * projet d'écriture à quatre mains
    * publications en bloc le 18 mai 2010
  * **Instin textopoly**
    * résidence de création
    * juin 2013
  * **Conquête du pays Ugogo**
    * Festival et performances
    * publications en mai-juin 2014
    * 5 contributions + vidéos
  * **rue Instin**
    * festival à Belleville : 4-7 juin 2015
    * publications du 30 juin 2015 à septembre 2015
    * 23 contributions
  * **Spoon River**
    * projet de traduction du recueil de poésie «_Spoon River Anthology_» d'Edgar Lee Masters (1915)
      * "traduit par la mouvance Général Instin"
      * publié chez Le Nouvel Attila - collection Othello (comme Climax)
    * de octobre 2016 au 1er mars 2017

## CLIMAX

(à venir)

## AUTRES

Notamment sur facebook, on trouve une catégorie de photo INSTIN "non-officiel", manifestations sur les murs (tags, graffs, etc.) du phénomène GI, avec la campagne "officielle" menée avec l'artiste SP38, et une campagne d'affichage "non officielle" _"à l'insu du général"_, réalisée grâce à une série de contributions anonymes.

## Arbres et rhizome

Elle n'est ni formelle, ni complète, mais cette ébauche nous rassure. Elle nous laisse penser que GI est un ensemble fini. Avec un nombre d'auteurs, de contributions, de plateformes maîtrisables. Elle nous montre par ailleurs que le rhizome est en fait tout à fait organisé et distribué dans des rubriques identifiées. Il y a là deux organisations qui se font face : celle arborescente des plateformes (voir les rubriques de Remue.net), et celle rhizomatique des textes hyperliées. La représentation/visualisation de cette dernière structuration constituera évidemment un excellent chantier pour étudier le corpus.

Malgré tout, elle nous rappelle à l'ordre sur le fait que la littérature brouhaha ne se laisse pas dompter aussi facilement, et qu'en tentant de l'appréhender, nous laisserons nécessairement de côté certains de ses recoins avec le risque de générer des angles morts.
