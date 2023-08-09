---
title: Reading
layout: page
---

This is a copy (and slight extension) of [my goodreads list](https://www.goodreads.com/max_barners).

My ratings: 5 is "Really good"; 4 is "Good"; 3 is "Okay"; 2 is "Bad"; 1 is "Really bad". The rating is imprecise on purpose. Here's a <a href="/reading/five-stars/">list of all the books I've rated five stars</a>.

<h2>2023</h2>

<ol reversed>
{% for book in site.data.books2023 %}
	<li {% if book.my_rating == 5 %}class="five-star"{% endif %}>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, <span class="rating">rated {{ book.my_rating }}/5</span>.
		{%- endif-%}
		{%- if book.my_notes -%}
		&nbsp;<a href="{{ book.my_notes }}">My notes<span class="sr-only">on {{ book.title }}</span></a>.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>Earlier</h2>

<ul>
	<li><a href="/reading/2022">2022</a></li>
	<li><a href="/reading/2021">2021</a></li>
	<li><a href="/reading/2020">2020</a></li>
	<li><a href="/reading/2019">2019</a></li>
	<li><a href="/reading/2018">2018</a></li>
	<li><a href="/reading/2017">2017</a></li>
</ul>

<p>Long list of <a href="/reading/all">all the books I've read since 2017</a>.</p>