---
title: Reading
layout: page
---

Here's a list of <a href="/reading/five-stars/">all the books I've rated five stars</a>. That means "really good"; marked with a ★ below.

<!--
{%- assign booksthisyear = site.data.books2025.size -%}
{%- assign bookspermonthmonth = site.time | date: "%-m" -%}
{% assign bookspermonth = booksthisyear | divided_by: bookspermonthmonth | round %}
{% assign rereads = site.data.books2025 | where: "reread", "true" %}

<p>📚 Books read this year: {{ booksthisyear }}. 🎶 Average bpm: {{ bookspermonth }}. ⏪ Rereads: {{ rereads.size }}.</p>

{%- assign Fiction = site.data.books2025 | where: "genre", "Fiction" -%}
{%- assign ScienceFiction = site.data.books2025 | where: "genre", "Science Fiction" -%}
{%- assign Fantasy = site.data.books2025 | where: "genre", "Fantasy" -%}
{%- assign Poetry = site.data.books2025 | where: "genre", "Poetry" -%}
{%- assign Buddhism = site.data.books2025 | where: "genre", "Buddhism" -%}
{%- assign Zen = site.data.books2025 | where: "genre", "Zen" -%}
{%- assign Nonduality = site.data.books2025 | where: "genre", "Nonduality" -%}
{%- assign Philosophy = site.data.books2025 | where: "genre", "Philosophy" -%}
{%- assign Taoism = site.data.books2025 | where: "genre", "Taoism" -%}
{%- assign Stoicism = site.data.books2025 | where: "genre", "Stoicism" -%}
{%- assign Nonfiction = site.data.books2025 | where: "genre", "Nonfiction" -%}
{%- assign Accessibility = site.data.books2025 | where: "genre", "Accessibility" -%}

{%- assign totalFiction = Fiction.size | plus: ScienceFiction.size | plus: Fantasy.size -%}
{%- assign totalPhilosophy = Buddhism.size | plus: Zen.size | plus: Nonduality.size | plus: Philosophy.size | plus: Taoism.size | plus: Stoicism.size -%}
{%- assign totalOther = booksthisyear | minus: totalFiction | minus: totalPhilosophy -%}

🎭 Genre stats:
Fiction: {{ Fiction.size }};
Science Fiction: {{ ScienceFiction.size }};
Fantasy: {{ Fantasy.size }};
Poetry: {{ Poetry.size }};
Buddhism: {{ Buddhism.size }};
Zen: {{ Zen.size }};
Nonduality: {{ Nonduality.size }};
Philosophy: {{ Philosophy.size }};
Taoism: {{ Taoism.size }};
Stoicism: {{ Stoicism.size }};
Nonfiction: {{ Nonfiction.size }};
Accessibility: {{ Accessibility.size }}.<br>
Broad summary: 
Fiction: {{ totalFiction }};
Philosophy: {{ totalPhilosophy }};
Other: {{ totalOther }}.
-->

{% assign thisMonth = site.data.books2025[0].date_read | date: "%m" %}
{% assign siteMonth = site.time | date: "%m" %}
{% if thisMonth == siteMonth %}
<h2>{{ site.time | date: "%B" }}</h2>
{% endif %}

<ol reversed>
{%- assign previousMonth = site.time | date: "%m" -%}

{% for book in site.data.books2025 %}

{%- assign currentMonth = book.date_read | date: "%m" -%}
{% if currentMonth != previousMonth %}
</ol>

<h2>{{ book.date_read | date: "%B" }}</h2>
<ol reversed>
{%- assign previousMonth = currentMonth -%}
{% endif %}

	<li class="{% if book.fivestar %} five-star{% endif %}{% if currentMonth != previousMonth %} month-change{%- assign previousMonth = currentMonth -%}{% endif %}">
		{% if book.fivestar %}★ {% endif %}
		<span class="title">{{ book.title }}</span> by <span class="author">{{ book.author }}</span>.
		<span class="genre">{{ book.genre }}</span>.
		<span class="read">{%- if book.reread -%}(Re)re{%- else -%}Re{%- endif -%}ad {{ book.date_read | date: "%d-%m-%Y" }}.</span>
		{%- if book.my_notes -%}
		&nbsp;<a href="{{ book.my_notes }}">My notes<span class="sr-only">on {{ book.title }}</span></a>.
		{%- endif-%}
	</li>
{% endfor %}
</ol>

<h2>Earlier</h2>

<ul>
	<li><a href="/reading/2024/">2024</a></li>
	<li><a href="/reading/2023/">2023</a></li>
	<li><a href="/reading/2022/">2022</a></li>
	<li><a href="/reading/2021/">2021</a></li>
	<li><a href="/reading/2020/">2020</a></li>
	<li><a href="/reading/2019/">2019</a></li>
	<li><a href="/reading/2018/">2018</a></li>
	<li><a href="/reading/2017/">2017</a></li>
</ul>

<p>Long list of <a href="/reading/all">all the books I've read since 2017</a>.</p>