---
title: Reading - five stars
layout: page
---

<p>Books that I've rated 5/5: really good.</p>

<h2>2025</h2>

<ol reversed>
{% for book in site.data.books2025 %}
	{%- if book.fivestar -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2024</h2>

<ol reversed>
{% for book in site.data.books2024 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2023</h2>

<ol reversed>
{% for book in site.data.books2023 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2022</h2>

<ol reversed>
{% for book in site.data.books2022 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2021</h2>

<ol reversed>
{% for book in site.data.books2021 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2020</h2>

<ol reversed>
{% for book in site.data.books2020 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2019</h2>

<ol reversed>
{% for book in site.data.books2019 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2018</h2>

<ol reversed>
{% for book in site.data.books2018 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>

<h2>2017</h2>

<ol reversed>
{% for book in site.data.books2017 %}
	{%- if book.my_rating == 5 -%}
	<li>
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>. Read {{ book. date_read | date: "%d-%m-%Y" }}.
	</li>
	{%- endif -%}
{% endfor %}
</ol>
