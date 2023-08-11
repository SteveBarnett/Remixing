---
title: This week
layout: page
---

{% assign currentYear = site.time | date: "%Y" %}
{% assign currentWeek = site.time | date: "%U" %}

<h2 id="thinking">Thinking</h2>

<ol>

{%- assign thinkingposts = site.thinking | limit: 50 | sort: "updated" | reverse -%}

{% for thinkingpost in thinkingposts %}
    {% unless thinkingpost.longerform %}

    {%- assign thinkingPostYear = thinkingpost.updated | date: "%Y" -%}
    {%- assign thinkingPostWeek = thinkingpost.updated | date: "%U" -%}

    {%- if currentYear == thinkingPostYear and currentWeek == thinkingPostWeek -%}
        <li>
            <a href="{{ thinkingpost.url }}">{{ thinkingpost.title }}</a>
            (added {{ thinkingpost.added }}{% if thinkingpost.updated != thinkingpost.added %}, updated {{ thinkingpost.updated }}{% endif %})
        </li>
    {% endif %}

    {% endunless %}
{% endfor %}

{%- assign longerformposts = site.thinking | where: "longerform", "true" | sort: "updated" | reverse -%}

{% for longerformpost in longerformposts %}

    {%- assign longerFormPostYear = longerformpost.updated | date: "%Y" -%}
    {%- assign longerFormPostWeek = longerformpost.updated | date: "%U" -%}

    {%- if currentYear == longerFormPostYear and currentWeek == longerFormPostWeek -%}

    <li>
        <a href="{{ longerformpost.url }}">{{ longerformpost.title }}</a>
        (added {{ longerformpost.added }}{% if longerformpost.updated !=  longerformpost.added %}, updated {{ longerformpost.updated }}{% endif %})
    </li>

  {% endif %}
{% endfor %}

{%- assign recentposts = site.posts | limit: 50 -%}
{%- assign reversedRecentPosts = recentposts | reverse -%}

{%- for recentpost in reversedRecentPosts -%}
    
	{%- assign recentPostYear = recentpost.date | date: "%Y" -%}
	{%- assign recentPostWeek = recentpost.date | date: "%U" -%}

    {%- if currentYear == recentPostYear and currentWeek == recentPostWeek -%}

    <li>
        {%- if recentpost.star -%}<strong>{%- endif -%}
        {{ recentpost.title }} 
        {%- if recentpost.star -%}</strong>{%- endif -%}
        <span class="tags">&nbsp;In&nbsp;

        {%- assign sortedrecentposttags = recentpost.tags | sort_natural -%}

        {%- capture recentposttags -%}
          {%- for tag in sortedrecentposttags -%}
          , <span class="tagmoji">{{ site.data.tagmoji[tag] }}</span>&nbsp;<a href="/thinking/all/#{{ tag }}">{{ tag | capitalize }}</a>
          {%- endfor -%}
        {%- endcapture -%}

        {{ recentposttags | remove_first: ", " }}. Added {{ recentpost.date | date: "%d-%m-%Y" }}.</span>
    </li>
    {%- endif -%}
    
{%- endfor -%}

</ol>

<h2 id="noting">Noting</h2>

<ul>

{%- assign notes = site.static_files | sort: "modified_time" | reverse | where_exp: "file", "file.path contains '/notes/'" -%}
    {%- for note in notes -%}
        {%- assign currentNoteYear = note.modified_time | date: "%Y" -%}
        {%- assign currentNoteWeek = note.modified_time | date: "%U" -%}

        {%- if currentYear == currentNoteYear and currentWeek == currentNoteWeek -%}
        <li>
          <a href="{{ note.path }}">
            {{ note.basename }}
          </a>
          <span class="hidden">
            currentYear: {{ currentYear }},
            currentNoteYear: {{ currentNoteYear}},
            currentWeek: {{ currentWeek }},
            currentNoteWeek: {{ currentNoteWeek}},
            note.modified_time: {{ note.modified_time }}
          </span>
        </li>
        {%- endif -%}
    {%- endfor -%}
</ul>

<h2 id="reading">Reading</h2>

<ol>
{%- for book in site.data.books2023 -%}
    {%- assign currentBookWeek = book.date_read | date: "%U" -%}
    {%- if currentWeek == currentBookWeek -%}
        <li>
            {{ book.title }} by {{ book.author }}. Read {{ book. date_read | date: "%d-%m-%Y" }}
            {%- if book.my_rating == 0 -%}
            .
            {%- else -%}
            , rated {{ book.my_rating }}/5.
            {%- endif-%}
            {%- if book.my_notes -%}
            &nbsp;<a href="{{ book.my_notes }}">My notes<span class="sr-only">on {{ book.title }}</span></a>.
            {%- endif-%}
        </li>
    {%- endif-%}
{%- endfor -%}
</ol>
