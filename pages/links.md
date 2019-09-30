---
layout: page
title: ΣΥΝΔΕΣΜΟΙ
feature-img: files/1.jpg
nav_weight: 3
permalink: /συνδεσμοι/
---
<div id="links">
<ul class="nav nav-pills" role="tablist">
    <li class="nav-item">
      <a class="nav-link active" data-toggle="pill" href="#menu5">Ε.Φ.Κ.Α</a>
    </li>
    <li class="nav-item">
      <a class="nav-link " data-toggle="pill" href="#home">Πανεπιστήμια</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="pill" href="#menu1">Σύλλογοι</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="pill" href="#menu2"> Περιοδικά</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="pill" href="#menu3">Διεθνείς Οργανισμοί</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="pill" href="#menu4"> Επιστημονικές Εταιρίες</a>
    </li>
  </ul>



<div class="tab-content">
    <div id="home" class="container tab-pane fade"><br>       
     {% assign links = site.data.useful_links.University | sort: 'link_name' %}
<ul>
{% for link in links %}
  <li>
<a href="{{ link.link_url }}">{{ link.link_name }}</a>
  </li>
{% endfor %}
</ul>
     </div>


  <div id="menu1" class="container tab-pane fade"><br>
       {% assign links = site.data.useful_links.Dental_Association | sort: 'link_name' %}
<ul>
{% for link in links %}
  <li>
<a href="{{ link.link_url }}">{{ link.link_name }}</a>
  </li>
{% endfor %}
</ul>
    </div>




    <div id="menu2" class="container tab-pane fade"><br>
      {% assign links = site.data.useful_links.Journal | sort: 'link_name' %}
<ul>
{% for link in links %}
  <li>
<a href="{{ link.link_url }}">{{ link.link_name }}</a>
  </li>
{% endfor %}
</ul>    
    </div>


<div id="menu3" class="container tab-pane fade"><br>
      {% assign links = site.data.useful_links.International_Association | sort: 'link_name' %}
<ul>
{% for link in links %}
  <li>
<a href="{{ link.link_url }}">{{ link.link_name }}</a>
  </li>
{% endfor %}
</ul>    
</div>

<div id="menu4" class="container tab-pane fade"><br>
{% assign links = site.data.useful_links.Gr_Association | sort: 'link_name' %}
<ul>
{% for link in links %}
  <li>
<a href="{{ link.link_url }}">{{ link.link_name }}</a>
  </li>
{% endfor %}
</ul>    
</div>

<div id="menu5" class="container tab-pane active"><br>
{% assign links = site.data.useful_links.Gr_Gov | sort: 'link_name' %}
<ul>
{% for link in links %}
  <li>
<a href="{{ link.link_url }}">{{ link.link_name }}</a>
  </li>
{% endfor %}
</ul>    
</div>









  </div>
</div>















  
  
  