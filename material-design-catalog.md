---
layout: page
title: Material Design Catalog
extra_css:
  - /css/catalog.css
sidebar: home_sidebar
permalink: /material-design-catalog/
---

This page catalogs Flutter’s reference implementation of UI components from Google’s [Material Design Specification](https://material.google.com/).
You can see many of the material design widgets in action in our [Flutter Gallery](https://github.com/flutter/flutter/tree/master/examples/flutter_gallery) demo app.

Flutter makes material design easy to implement, but you don't need to use material design in your app.
Flutter's base widgets provide extensible starting points to build customer UIs with Flutter. To learn more, check out the [Basic Widgets Overview](/basic-widgets/).

<!-- Data for the catalog comes from catalog.csv in the _data folder -->
{% for comp in site.data.catalog %}
<div class="comp-entry">
  <h2>{{comp.comp_name}}</h2>
  <img class="comp-img" src="{{comp.img_link}}"/>
  <p>
   {{comp.comp_desc}}
   {% if comp.widget_name != '' %}
     The <a href="{{comp.dartdocs_link}}">{{comp.widget_name}}</a> widget implements this component.
   {% endif %}
   {{comp.extra_html}}
  </p>
  <p><a href="https://github.com/flutter/flutter/search?utf8=%E2%9C%93&q=path%3Aexamples+{{comp.keywords}}&type=Code">Sample usage</a>
  | <a href="{{comp.dartdocs_link}}">Documentation</a>
  | <a href="{{comp.material_spec_link}}">Interface design guidelines</a>
</div>
{% endfor %}

<div class="catalog-end"></div>
