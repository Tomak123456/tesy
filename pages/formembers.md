---
title: ΑΝΑΚΟΙΝΩΣΕΙΣ
layout: page
feature-img: files/1.jpg
nav_weight: 2
permalink: /ανακοινωσεις/
---
<div style="min-height: 440px;">

<h3 class="my-auto">Αγγελίες</h3>
<hr>
<ul>
 {% assign sorted = (site.aggelies | sort: 'date') | reverse %}
  {% for item in sorted limit:10 %}
    <li>
      <a href="{{site.baseurl}}{{ item.url }}">{{ item.title }}</a>
      
    </li>
  {% endfor %}
</ul>

<h3 class="my-auto">Ασφάλιση</h3>
<hr>
<ul>
 {% assign sorted = (site.insurance | sort: 'date') | reverse %}
  {% for item in sorted limit:10 %}
    <li>
      <a href="{{site.baseurl}}{{ item.url }}">{{ item.title }}</a>
      
    </li>
  {% endfor %}
</ul>

<h3 class="my-auto">Δικαιολογητικά</h3>
<hr>
<ul>
 {% assign sorted = (site.supportingdocuments | sort: 'date') | reverse %}
  {% for item in sorted limit:10 %}
    <li>
      <a href="{{site.baseurl}}{{ item.url }}">{{ item.title }}</a>
      
    </li>
  {% endfor %}
</ul>

<h3>Εκδηλώσεις</h3>
<hr>
<ul>
 {% assign sorted = (site.events | sort: 'date') | reverse %}
  {% for itemm in sorted limit:10 %}
    <li>
      <a href="{{site.baseurl}}{{ itemm.url }}">{{ itemm.title }}</a>
     
    </li>
  {% endfor %}
</ul>
<h3>Νομοθεσία ΦΕΚ</h3>
<hr>
  <ul>
  {% assign sorted = (site.laws | sort: 'date') | reverse %}
  {% for animal in sorted limit:10 %}
    <li>
      <a href="{{site.baseurl}}{{ animal.url }}">{{ animal.title }}</a>
      
    </li>
  {% endfor %}
</ul> 
<h3>Νέα</h3>
<hr>
  <ul>
  {% assign sorted = (site.news | sort: 'date') | reverse %}
  {% for animall in sorted limit:10 %}
    <li>
      <a href="{{site.baseurl}}{{ animall.url }}">{{ animall.title }}</a>
      
    </li>
  {% endfor %}
</ul>











</div>