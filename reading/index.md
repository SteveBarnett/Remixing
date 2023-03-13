---
title: Reading
layout: page
---

This is a copy of [my goodreads list](https://www.goodreads.com/max_barners).

<h2>2023</h2>

<ol reversed>
{% for book in site.data.books2023 %}
	<li {% if book.my_rating == 5 %}class="five-star"{% endif %}>
		<strong>{{ book.title }}</strong> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, <span class="rating">rated {{ book.my_rating }}/5</span>.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>2022</h2>

<ol reversed>
{% for book in site.data.books2022 %}
	<li>
		<strong>{{ book.title }}</strong> by {{ book.author }}. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, rated {{ book.my_rating }}/5.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>2021</h2>

<ol reversed>
{% for book in site.data.books2021 %}
	<li>
		<strong>{{ book.title }}</strong> by {{ book.author }}. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, rated {{ book.my_rating }}/5.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>2020</h2>

<ol reversed>
{% for book in site.data.books2020 %}
	<li>
		<strong>{{ book.title }}</strong> by {{ book.author }}. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, rated {{ book.my_rating }}/5.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>2019</h2>

<ol reversed>
{% for book in site.data.books2019 %}
	<li>
		<strong>{{ book.title }}</strong> by {{ book.author }}. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, rated {{ book.my_rating }}/5.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>2018</h2>

<ol reversed>
{% for book in site.data.books2018 %}
	<li>
		<strong>{{ book.title }}</strong> by {{ book.author }}. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, rated {{ book.my_rating }}/5.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>2017</h2>

<ol reversed>
{% for book in site.data.books2017 %}
	<li>
		<strong>{{ book.title }}</strong> by {{ book.author }}. Read {{ book. date_read | date: "%d-%m-%Y" }}
		{%- if book.my_rating == 0 -%}
		.
		{%- else -%}
		, rated {{ book.my_rating }}/5.
		{%- endif-%}
	</li>
{% endfor %}
</ol>
