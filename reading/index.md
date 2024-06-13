---
title: Reading
layout: page
---

This is a copy (and slight extension) of [my goodreads list](https://www.goodreads.com/max_barners).

My ratings: 5 is "Really good"; 4 is "Good"; 3 is "Okay"; 2 is "Bad"; 1 is "Really bad". The rating is imprecise on purpose. Here's a <a href="/reading/five-stars/">list of all the books I've rated five stars</a>.

{% assign thisMonth = site.data.books2024[0].date_read | date: "%m" %}
{% assign siteMonth = site.time | date: "%m" %}
{% if thisMonth == siteMonth %}
<h2>{{ site.time | date: "%B" }}</h2>
{% endif %}

<ol reversed>
{%- assign previousMonth = site.time | date: "%m" -%}

{% for book in site.data.books2024 %}

{%- assign currentMonth = book.date_read | date: "%m" -%}
{% if currentMonth != previousMonth %}
</ol>

<h2>{{ book.date_read | date: "%B" }}</h2>
<ol reversed>
{%- assign previousMonth = currentMonth -%}
{% endif %}

	<li class="{% if book.my_rating == 5 %} five-star{% endif %}{% if currentMonth != previousMonth %} month-change{%- assign previousMonth = currentMonth -%}{% endif %}">
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>.
		<span class="genre">{{ book.genre }}</span>.
		<span class="read">Read {{ book.date_read | date: "%d-%m-%Y" }}.</span>
		<span class="rating">Rated {{ book.my_rating }}/5</span>.
		{%- if book.my_notes -%}
		&nbsp;<a href="{{ book.my_notes }}">My notes<span class="sr-only">on {{ book.title }}</span></a>.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>Earlier</h2>

<ul>
	<li><a href="/reading/2023">2023</a></li>
	<li><a href="/reading/2022">2022</a></li>
	<li><a href="/reading/2021">2021</a></li>
	<li><a href="/reading/2020">2020</a></li>
	<li><a href="/reading/2019">2019</a></li>
	<li><a href="/reading/2018">2018</a></li>
	<li><a href="/reading/2017">2017</a></li>
</ul>

<p>Long list of <a href="/reading/all">all the books I've read since 2017</a>.</p>