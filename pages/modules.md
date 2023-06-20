---
title: Modules
nav: Modules
nav_order: 2
section: Modules
section-color: success
layout: page
---

<div class="container content-narrow pb-2" markdown="1">

## Purpose:

Modules introduce basic concepts in static web development, including GitHub, HTML, Markdown, data concepts, and computational methods.

## Format:

- Modules are written in markdown files hosted on GitHub for easy copying and reuse.
- Each module takes 30 minutes or less to complete.

## Use Cases:
- Assign one or more modules as homework for students before beginning a static web project in the classroom
- Combine modules into a sequential workshop or class session

</div>

<hr>

## Browse Modules

<div class="row pt-2">
{%- for m in site.data.modules -%}
<div class="col-md-4">
    <div class="card my-2">
    <div class="card-body">
        <h4 class="card-title"><a href="{{ m.link }}" target="_blank" rel="noopener">{{ m.title}}</a></h4>
        <p class="card-text"><strong>Skills:</strong> {{ m.skills }}<br>
        <p class="card-text">{{ m.description }}</p>
    </div>
    </div>
</div>
{% endfor %}
</div>