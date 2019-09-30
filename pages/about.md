---
layout: page
title: "ΔΙΟΙΚΗΤΙΚΟ ΣΥΜΒΟΥΛΙΟ"
feature-img: files/1.jpg
nav_weight: 1
permalink: /διοικητικο-συμβουλιο/
---

<div class="container">
        <div class="row">
          <div class="col-lg-12 text-center">
            <h2 class="section-heading">Διοικητικό Συμβούλιο</h2>
            <hr class="my-4">
          </div>
        </div>
      </div>

<div class="container">
<div class="row justify-content-md-center">

 {% for member in site.data.ds %}


<div class="card mb-2 ml-2 shadow-sm" style="width: 18rem;" >
  <div class="card-body">
    <h5 class="card-title text-primary">{{ member.position }}</h5>
    <h3 class="card-subtitle mb-2 text-muted"></h3>
    <p class="card-text font-weight-bold">{{ member.name }} {{member.lastname}}</p>
    <a href="https://maps.google.com/?q={{member.city}},{{member.location}}">{{member.location}}</a>
    <a class="btn d-block" href="tel:{{member.mobile}}">{{member.mobile}}</a>
    
  </div>
</div>
{% endfor %}

</div>      
</div>      


