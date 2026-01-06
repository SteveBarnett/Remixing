---
title: Reading
layout: page
books: books2026
---

Here's a list of <a href="/reading/five-stars/">all the books I've rated "really good"</a>, marked with a ★ below. [Jump to reading lists](#reading-lists).

{%- assign booksthisyearcount = site.data[page.books].size -%}
{%- assign bookspermonthmonth = site.time | date: "%-m" -%}
{% assign bookspermonth = booksthisyearcount | divided_by: bookspermonthmonth | round %}
{% assign rereads = site.data[page.books] | where: "reread", "true" %}
{% assign fivestar = site.data[page.books] | where: "fivestar", "true" %}

<ul>

<li>
📚 Books read this year: {{ booksthisyearcount }}. 🎶 Average bpm: {{ bookspermonth }}. 🌟 Five stars: {{ fivestar.size }}. ⏪ Rereads: {{ rereads.size }}.
</li>

{%- assign Fiction = site.data[page.books] | where: "genre", "Fiction" -%}
{%- assign ScienceFiction = site.data[page.books] | where: "genre", "Science Fiction" -%}
{%- assign Fantasy = site.data[page.books] | where: "genre", "Fantasy" -%}
{%- assign Poetry = site.data[page.books] | where: "genre", "Poetry" -%}
{%- assign Buddhism = site.data[page.books] | where: "genre", "Buddhism" -%}
{%- assign Zen = site.data[page.books] | where: "genre", "Zen" -%}
{%- assign Nonduality = site.data[page.books] | where: "genre", "Nonduality" -%}
{%- assign Philosophy = site.data[page.books] | where: "genre", "Philosophy" -%}
{%- assign Taoism = site.data[page.books] | where: "genre", "Taoism" -%}
{%- assign Stoicism = site.data[page.books] | where: "genre", "Stoicism" -%}
{%- assign Nonfiction = site.data[page.books] | where: "genre", "Nonfiction" -%}
{%- assign Accessibility = site.data[page.books] | where: "genre", "Accessibility" -%}

{%- assign totalFiction = Fiction.size | plus: ScienceFiction.size | plus: Fantasy.size -%}
{%- assign totalPhilosophy = Buddhism.size | plus: Zen.size | plus: Nonduality.size | plus: Philosophy.size | plus: Taoism.size | plus: Stoicism.size -%}
{%- assign totalOther = booksthisyearcount | minus: totalFiction | minus: totalPhilosophy -%}

<li>
🎭 Genre stats:&nbsp;
{%- unless Fiction.size == 0 -%}Fiction: {{ Fiction.size }};&nbsp;{%- endunless -%}
{%- unless ScienceFiction.size == 0 -%}Science Fiction: {{ ScienceFiction.size }};&nbsp;{%- endunless -%}
{%- unless Fantasy.size == 0 -%}Fantasy: {{ Fantasy.size }};&nbsp;{%- endunless -%}
{%- unless Poetry.size == 0 -%}Poetry: {{ Poetry.size }};&nbsp;{%- endunless -%}
{%- unless Buddhism.size == 0 -%}Buddhism: {{ Buddhism.size }};&nbsp;{%- endunless -%}
{%- unless Zen.size == 0 -%}Zen: {{ Zen.size }};&nbsp;{%- endunless -%}
{%- unless Nonduality.size == 0 -%}Nonduality: {{ Nonduality.size }};&nbsp;{%- endunless -%}
{%- unless Philosophy.size == 0 -%}Philosophy: {{ Philosophy.size }};&nbsp;{%- endunless -%}
{%- unless Taoism.size == 0 -%}Taoism: {{ Taoism.size }};&nbsp;{%- endunless -%}
{%- unless Stoicism.size == 0 -%}Stoicism: {{ Stoicism.size }};&nbsp;{%- endunless -%}
{%- unless Accessibility.size == 0 -%}Accessibility: {{ Accessibility.size }};&nbsp;{%- endunless -%}
{%- unless Nonfiction.size == 0 -%}Nonfiction: {{ Nonfiction.size }}.{%- endunless -%}
</li>

<li>
📊 Broad summary: 
Philosophy: {{ totalPhilosophy }};
Fiction: {{ totalFiction }};
Other: {{ totalOther }}.
</li>

</ul>

{% include search-form.html title=page.title %}

{% assign thisMonth = site.data[page.books][0].date_read | date: "%m" %}
{% assign siteMonth = site.time | date: "%m" %}
{% if thisMonth == siteMonth %}
<h2>{{ site.time | date: "%B" }}</h2>
{% endif %}

<ol reversed>
{%- assign previousMonth = site.time | date: "%m" -%}

{% for book in site.data[page.books] %}

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
	<li><a href="/reading/2025/">2025</a></li>
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

## Reading lists

- Fiction: [holds at the library](https://libbyapp.com/shelf/holds)
- Fiction: [toreadmaybe + fiction Pinboard bookmarks](https://pinboard.in/u:maxbarners/t:toreadmaybe/t:fiction/)
- Nonfiction: [toreadmaybe + nonfiction Pinboard bookmarks](https://pinboard.in/u:maxbarners/t:toreadmaybe/t:nonfiction/)
- Buddhism (and related, like mindfulness): [toreadmaybe + buddhism Pinboard bookmarks](https://pinboard.in/u:maxbarners/t:toreadmaybe/t:buddhism/)
- Zen (and related, like Daoism): [toreadmaybe + zen Pinboard bookmarks](https://pinboard.in/u:maxbarners/t:toreadmaybe/t:zen/)
- Philosophy: [toreadmaybe + philosophy Pinboard bookmarks](https://pinboard.in/u:maxbarners/t:toreadmaybe/t:philosophy/)
- Stoicism: [toreadmaybe + stoicism Pinboard bookmarks](https://pinboard.in/u:maxbarners/t:toreadmaybe/t:stoicism/)

{% include search-js.html %}
