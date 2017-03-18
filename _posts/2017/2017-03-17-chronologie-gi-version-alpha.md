---
layout: post
title: Chronologie GI (version alpha)
date: '2017-03-17 22:18'
tags: 'visualisation, data, méthode'
---

Notre archive n'est pas encore terminée que nous ne pouvons nous empêcher de produire quelques visualisations. Voici un tout premier test de chronologie à partir d'un simple extrait de l'archive, en utilisant [la timeline JS du Knight Lab](https://timeline.knightlab.com/).

Ce petit exercice a plusieurs atouts :

1. de produire un résulat visuel et esthétique tout à fait satisfaisant après des semaines à collecter des données et à générer une archive XML peu digeste,
2. de procéder à un nettoyage des données et d'identifier certaines données manquantes,
3. d'explorer un échantillon de l'archive sous une nouvelle perspective : celle de la distribution dans le temps et par rubrique.

Ce dernier point n'est pas anodin car il marque une première étape à partir de laquelle nous allons (enfin) pouvoir itérer notre problématique, nos objectifs, l'archive et sa modélisation, et finalement procéder à de nouvelles requêtes sur l'archive. La fouille de données consiste toujours en une démarche itérative, mettant en dialogue des hypothèses (requêtes) et un corpus (résultats).

## Chronologie GI sur Remue.net
<iframe src='https://cdn.knightlab.com/libs/timeline3/latest/embed/index.html?source=1Xn7o0mun9Z9qYM-g2XGyT-37uvrAHRqtw2KX3rvCzgM&font=Default&lang=fr&initial_zoom=2&height=650' width='100%' height='650' webkitallowfullscreen mozallowfullscreen allowfullscreen frameborder='1'></iframe>

## Workflow

Nous utilisons [BaseX](http://basex.org/) pour exploiter l'archive XML TEI. Dans cette phase exploratoire, cela nous permet de parcourir les contenus et les métadonnées très efficacement. Il suffit parfois d'une simple fonction Xquery, ou parfois d'un script minimal pour produire une liste de résultats que l'on peut ensuite exploiter plus finement.

Pour le présent exercice, [ce script](#script-de-conversion-xml-to-csv) sélectionne les données pertinentes pour la chronologie, puis convertit le nouvel arbre xml en un fichier csv. Timeline JS permet de publier une chronologie [à partir d'un simple fichier csv](https://timeline.knightlab.com/index.html#make) sur Google Spreadsheet.


---

### Script de conversion XML to CSV

~~~~~~
xquery version "3.1";

declare default function namespace 'local' ;
declare namespace csv = "http://basex.org/modules/csv";


let $options := map { 'separator': ';'}

let $TEI := db:open("GITEI2")
(: declare function local:getItemList( $TEI as element() ) as element()* { :)

let $toBeCsv :=  <itemList>{
  for $item in $TEI/TEI
    let $title := $item//title
    let $author := $item//author
    let $date := fn:string($item//publicationStmt/date/@when)
    let $rubrique := $item//publicationStmt/category
  return
  <item>
    <year>{fn:substring($date,1,4)}</year>
    <month>{fn:substring($date,6,2)}</month>
    <day>{fn:substring($date,9,2)}</day>
    <time></time>
    <endYear></endYear>
    <endMonth></endMonth>
    <endDay></endDay>
    <endTime></endTime>
    <displayDate></displayDate>
    {$title}
    {$author}
    <media></media>
    <mediaCredit></mediaCredit>
    <mediaCaption></mediaCaption>
    <type></type>
    <mediaThumbnail></mediaThumbnail>
    {$rubrique}
    <background></background>
  </item>
  }</itemList>

let $output := csv:serialize($toBeCsv, $options)
(: return $toBeCsv :)
(: return $output :)
return
    file:write-text("/path/teicsv.csv", $output)
~~~~~~
