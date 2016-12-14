---
layout: default
title: Home
---

<div style="padding: 50px 30px 30px 30px; background-color:beige; margin-bottom:30px">
  <p style="font-size:1.5em; font-weight:200"> Bienvenue sur le carnet de recherche <em>{{ site.title }}</em></p>
  <a class="btn btn-default btn-sm" href="{{ site.github.url }}/about" title="About">
    <i class="fa fa-arrow-right"></i> De quoi s'agit-il ?
  </a>
<hr/>
<!-- <h3 style="margin-top:20px">Dernières communications</h3>
  <ul class="fa-ul">
    <li><i class="fa-li fa fa-arrow-right"></i>au colloque <a href="http://www.iscc.cnrs.fr/spip.php?article2078" target="_blank" title="Colloque MIAu"><em>Médiations informatisées de l’autorité : nouvelles écritures, nouvelles pratiques de la reconnaissance ?</em></a><br>les 17 et 18 mars 2016 à l'ISCC (Paris)&nbsp;
    <a class="btn btn-default btn-sm" href="{{ site.github.url }}/2016/03/16/intervention-au-colloque-mediations-informatisees-de-l-autorite.html">
      <i class="fa fa-arrow-right"></i> intervention
    </a></li>
    <li><i class="fa-li fa fa-arrow-right"></i>au colloque <a href="http://colloque2016.ecrituresnumeriques.ca/" target="_blank"><em>Écrivains, personnages et profils : l’éditorialisation de l’auteur</em></a><br>les 24 et 25 mai 2016 à l'Université de Montréal.&nbsp;
    <a class="btn btn-default btn-sm" href="{{ site.github.url }}/2016/05/24/intervention-au-colloque-editorialisation-de-l-auteur.html">
      <i class="fa fa-arrow-right"></i> intervention
    </a></li>
  </ul> -->
</div>

<hr>
<div class="home">

  <h1 class="page-heading" style="margin-top:20px">Derniers posts :</h1>

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{% include date-fr.html date=post.date %}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.github.url }}">{{ post.title }}</a>
        </h2>
        {{ post.excerpt }}
        <hr>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.github.url }}">via RSS</a></p>

</div>
