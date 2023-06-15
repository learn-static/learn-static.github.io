---
title: Modules
nav: Modules
nav_order: 2
section: Modules
section-color: success
layout: page
#foot: js/browse-all.html
---

Learn-Static's five Learning Modules cover basic introductory concepts in static web development, including GitHub, HTML, Markdown, data concepts, and computational methods.
Modules are written in markdown files hosted on GitHub for easy copying and reuse.
Each module takes 30 minutes or less to complete.

**Use Cases**:
- Assign one or more modules as homework for students before beginning a static web project in the classroom
- Combine modules into a sequential workshop or class session

<div class="row">
{%- for m in site.data.modules -%}
<div class="col-md-4">
    <div class="card my-2">
    <div class="card-body">
        <h4 class="card-title"><a href="{{ m.link }}" target="_blank" rel="noopener">{{ m.title}}</a></h4>
        <p class="card-text"><strong>Skills:</strong> {{ m.skills }}</p>
        <p class="card-text">{{ m.description }}</p>
    </div>
    </div>
</div>
{% endfor %}
</div>

<!--
<div id="documentList">
    <div class="input-group mb-3">
        <input type="text" id="listSearch" class="form-control form-control-lg search" aria-label="Text input to filter list" placeholder="Filter...">
        <button class="btn btn-lg btn-outline-secondary dropdown-toggle" type="button" data-bs-toggle="collapse" data-bs-target="#collapseListOptions" aria-expanded="false" aria-controls="collapseListOptions">options</button>
        <div class="collapse w-100" id="collapseListOptions">
            <div class="card card-body">
                <p>Sort by:</p>
                <p>
                    <input type="radio" class="btn-check" name="sort_list" id="list_shuffle" autocomplete="off" checked>
                    <label class="btn btn-outline-info m-1" for="list_shuffle">Random</label>
                    <input type="radio" class="btn-check sort" name="sort_list" id="list_title" autocomplete="off" data-sort="listTitle">
                    <label class="btn btn-outline-info m-1" for="list_title">Title</label>
                    <input type="radio" class="btn-check sort" name="sort_list" id="list_type" autocomplete="off" data-sort="listType">
                    <label class="btn btn-outline-info m-1" for="list_type">Type</label>
                </p>
                <p>View item types:</p>
                <p>
                    <input type="radio" class="btn-check" name="filterRadio" id="filter-all" autocomplete="off" value="show-all" checked>
                    <label class="btn btn-outline-primary m-1" for="filter-all">All</label>
                    {% assign types = site.documents | where_exp: 'i','i.ignore != true' | map: 'type' | compact | uniq %}
                    {% for t in types %}
                    <input type="radio" class="btn-check" name="filterRadio" id="filter-{{ t | slugify }}" autocomplete="off" value="{{ t }}">
                    <label class="btn btn-outline-primary m-1" for="filter-{{ t | slugify }}">{{ t }}</label>
                    {% endfor %}
                </p>
            </div>
        </div>
    </div>
    <div class="mt-5 list row row-cols-1 row-cols-md-2"></div>
</div>
-->