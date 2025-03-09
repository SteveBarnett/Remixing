{% include header.html title=page.title %}

{{ content }}

{%- for category in site.categories reversed -%}
{%- if category[0] == "thinking" -%}
  {% continue %}
{% elsif category[0] == "doing" %}
  {% continue %}
{% elsif category[0] == "music" %}
  {% continue %}
{% else %}

<h2 id="{{ category[0] | downcase }}">Album: {{ category[0] }}</h2>

<ol reversed class="music">
  {%- for track in category[1] -%}
    <li>
      <audio controls preload="none" src="{{ track.url | replace: "-", " " }}.mp3">
          Your browser does not support the
          <code>audio</code> element.
      </audio>
      <a href="{{ track.url | replace: "-", " " }}.mp3">{{ track.title | downcase }}</a> ({{ track.date | date: "%Y-%m-%d" }})
  </li>
  {%- endfor -%}
</ol>

{%- endif -%}
{%- endfor -%}

{% include footer.html %}
