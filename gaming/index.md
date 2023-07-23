---
title: Gaming
layout: page
---

My ratings: 5 is "Really good"; 4 is "Good"; 3 is "Okay"; 2 is "Bad"; 1 is "Really bad". The rating is imprecise on purpose.

<h2>2023</h2>

<ol reversed>
{% for game in site.data.games2023 %}
	<li {% if game.my_rating == 5 %}class="five-star"{% endif %}>
		<span class="title">{{ game.title }}</span> on <span class="platform">{{ game.platform }}</span>. Played {{ game. date_played | date: "%d-%m-%Y" }}
		{%- if game.my_rating == 0 -%}
		.
		{%- else -%}
		, <span class="rating">rated {{ game.my_rating }}/5</span>.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<!--
<h2>Earlier</h2>

<ul>
	<li><a href="/reading/2023">2023</a></li>
</ul>
-->