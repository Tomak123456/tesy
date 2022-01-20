---
layout: page
title: ΟΔΟΝΤΙΑΤΡΟΙ
feature-img: files/1.jpg
nav_weight: 5
permalink: /οδοντιατροι-ορθοδοντικοι/τρικαλων/
---

{% assign dentists = site.documents | where:"layout", "profile" | where:"dentistspecialty", "Οδοντίατρος"   %}
    
{% assign ortho = site.documents | where:"layout", "profile" | where:"dentistspecialty", "Ορθοδοντικός"  %}



 <ul class="nav nav-pills" role="tablist">
    <li class="nav-item">
      <a class="nav-link active" data-toggle="pill" href="#home">Οδοντίατροι ({{dentists.size}})</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="pill" href="#menu1">Ορθοδοντικοί ({{ortho.size}})</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="modal" data-target="#myModal" href="#">
    <i class="fa fa-search"></i>
  </a>
    </li>
  </ul>



<div class="tab-content">
    <div id="home" class="container tab-pane active"><br>   
    
     {% assign dents = site.documents | where:"layout", "profile" | where:"dentistspecialty", "Οδοντίατρος" | sort: 'dentistname'  %}
             
      {% assign items_grouped = dents | group_by: 'dentistcity' | sort: "name" %}
      {% for group in items_grouped %}
    <h5>{{group.name}}</h5>
        {% for item in group.items %}
        <ul><a href="{{item.url}}">
            <li>{{item.dentistname}} {% if item.dentistmobile != null and item.dentistmobile != empty %}- {{item.dentistmobile}}{% endif %} {% if item.dentistaddress != null and item.dentistaddress != empty %}- {{item.dentistaddress}}{% endif %}{% if item.dentistspecialty != null and item.dentistspecialty != empty %} - {{item.dentistspecialty}}{% endif %}</li></a>
        </ul>
        {% endfor %}
    {% endfor %}
      </div>
    <div id="menu1" class="container tab-pane fade"><br>

 {% assign dents = site.documents | where:"layout", "profile" | where:"dentistspecialty", "Ορθοδοντικός" | sort: 'dentistname'  %}
    
    
    
    
    
    
    
     
      {% assign items_grouped = dents | group_by: 'dentistcity' | sort: "name" %}
      {% for group in items_grouped %}
    <h5>{{group.name}}</h5>
        {% for item in group.items %}
        <ul><a href="{{item.url}}">
            <li>{{item.dentistname}} {% if item.dentistmobile != null and item.dentistmobile != empty %}- {{item.dentistmobile}}{% endif %} {% if item.dentistaddress != null and item.dentistaddress != empty %}- {{item.dentistaddress}}{% endif %}{% if item.dentistspecialty != null and item.dentistspecialty != empty %} - {{item.dentistspecialty}}{% endif %}</li></a>
        </ul>
        {% endfor %}
    {% endfor %}


         </div>
</div>

{% include modalsearch.html %}
