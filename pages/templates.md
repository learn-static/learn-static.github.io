---
title: Templates
nav: Templates
nav_order: 3
section: Templates
section-color: warning
#foot: js/concepts.html
---

<div class="container content-narrow pb-2" markdown="1">

## Purpose:

Reusable static web code templates and documentation for projects that focus on teaching concepts around digital collections, oral histories, text analysis, and responsible data curation.

## Format:

Each project's template code is hosted in a GitHub repository and accompanied by example documentation and lesson plans that can be adapted to fit a specific classroom context or need.

## Use Cases:

Incorporate projects into a humanities or social science-focused classroom to enhance critical engagement with cultural material while also teaching transferable technical skills such as data management and web literacy.

</div>

<hr>

## Browse Templates

<div class="row pt-2">
{%- for t in site.data.templates -%}
<div class="col-md-4">
    <div class="card my-2">
    <div class="card-body">
        <h4 class="card-title">{{ t.title}}</h4>
        <p class="card-text"><strong>Topics:</strong> {{ t.topics }}</p>
        <p class="card-text">{{ t.description }}</p>
        <p class="card-text text-center">
        <a class="btn btn-outline-success btn-lg my-2 btn-custom" href="{{ t.repo-link }}">Code Template</a>
        <a class="btn btn-outline-warning btn-lg my-2 btn-custom" href="{{ t.demo-link }}">Demo Site</a>
        <a class="btn btn-outline-info btn-lg my-2" href="{{ t.docs-link }}">Project Documentation</a>
        </p>
    </div>
    </div>
</div>
{% endfor %}
</div>

<!--<div id="documentList">
    <div class="input-group mb-3">
        <input type="text" id="listSearch" class="form-control search" aria-label="Text input to filter list" placeholder="Filter...">
        <button class="btn btn-outline-secondary dropdown-toggle" type="button" data-bs-toggle="collapse" data-bs-target="#collapseListOptions" aria-expanded="false" aria-controls="collapseListOptions">options</button>
        <div class="collapse w-100" id="collapseListOptions">
            <div class="card card-body">
                <p>Sort by:</p>
                <p>
                    <input type="radio" class="btn-check" name="sort_list" id="list_shuffle" autocomplete="off" checked>
                    <label class="btn btn-outline-info m-1" for="list_shuffle">Random</label>
                    <input type="radio" class="btn-check sort" name="sort_list" id="list_title" autocomplete="off" data-sort="listTitle">
                    <label class="btn btn-outline-info m-1" for="list_title">Title</label>
                </p>
            </div>
        </div>
    </div>
    <div class="mt-5 list row row-cols-1 row-cols-md-2"></div>
</div>-->
