---
layout: page
title: Acceptance and resistance
sbcollection: true
added: 2023-12-03
updated: 2023-12-03
---

{%- assign acceptanceposts = site.posts | where: "acceptance", "true" | sort: "aandrorder" -%}

<ol>
  {%- for acceptance in acceptanceposts -%}
  <li id="{{ acceptance.title | truncatewords: 5 | slugify  }}">
    {{ acceptance.title }} <span class="tags">In
    
    {% assign sortedacceptance = acceptance.tags | sort_natural  %}

    {%- capture acceptancetags -%}
      {%- for tag in sortedacceptance -%}
      , <span class="tagmoji">{{ site.data.tagmoji[tag] }}</span>&nbsp;<a href="/{{ acceptance.categories[0] }}/all/#{{ tag }}">{{ tag | capitalize }}</a>
      {%- endfor -%}
    {%- endcapture -%}

    {{ acceptancetags | remove_first: ", " }}.</span>
  </li>
  {%- endfor -%}
</ol>
