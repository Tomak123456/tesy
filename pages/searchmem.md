---
layout: page
title: ΟΔΟΝΤΙΑΤΡΟΙ
feature-img: files/4.jpg
nav_weight: 5
permalink: /οδοντιατροι-ορθοδοντικοι/τρικαλων/
---

 <ul class="nav nav-pills" role="tablist">
    <li class="nav-item">
      <a class="nav-link active" data-toggle="pill" href="#home">Οδοντίατροι</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="pill" href="#menu1">Ορθοδο ντικοί</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" data-toggle="modal" data-target="#myModal" href="#">
    <i class="fa fa-search"></i>
  </a>
    </li>
  </ul>



<div class="tab-content">
    <div id="home" class="container tab-pane active"><br>
       {% assign dents = site.data.dent_members | where:"specialty","Οδοντίατρος" | sort: 'name' %} 
      {% assign items_grouped = dents | group_by: 'city' | sort: "name" %}
      {% for group in items_grouped %}
    <h5>{{group.name}}</h5>
        {% for item in group.items %}
        <ul>
            <li>{{item.name}} - <a href="tel:{{item.phone1}}">{{item.phone1}}</a> - {{item.address}} - {{item.specialty}}</li>
        </ul>
        {% endfor %}
    {% endfor %}
      </div>
    <div id="menu1" class="container tab-pane fade"><br>
      {% assign dents = site.data.dent_members | where:"specialty","Ορθοδοντικός" | sort: 'name' %} 
      {% assign items_grouped = dents | group_by: 'city' | sort: "name" %}
      {% for group in items_grouped %}
    <h5>{{group.name}}</h5>
        {% for item in group.items %}
        <ul>
            <li>{{item.name}} - <a href="tel:{{item.phone1}}">{{item.phone1}}</a> - {{item.address}} - {{item.specialty}}</li>
        </ul>
        {% endfor %}
    {% endfor %}
         </div>
</div>

{% include modalsearch.html %}
