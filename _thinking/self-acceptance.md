---
layout: page
title: Self-acceptance
sbcollection: true
added: 2023-08-13
updated: 2023-08-13
---

<h2>Human</h2>

{%- assign selfacceptancehumanposts = site.posts | where: "selfacceptancehuman", "true" | sort: "order" -%}

<ol>
	{%- for selfacceptancehumanpost in selfacceptancehumanposts -%}
		<li>
		{{ selfacceptancehumanpost.title }} <span class="tags">In

		{% assign sortedselfacceptancehumanpost = selfacceptancehumanpost.tags | sort_natural  %}

		{%- capture selfacceptancehumanposttags -%}
		  {%- for tag in sortedselfacceptancehumanpost -%}
		  , <span class="tagmoji">{{ site.data.tagmoji[tag] }}</span>&nbsp;<a href="/{{ selfacceptancehumanpost.categories[0] }}/all/#{{ tag }}">{{ tag | capitalize }}</a>
		  {%- endfor -%}
		{%- endcapture -%}

		{{ selfacceptancehumanposttags | remove_first: ", " }}.</span>
		</li>
	{%- endfor -%}
</ol>

<h2>Balance</h2>

{%- assign selfacceptancebalanceposts = site.posts | where: "selfacceptancebalance", "true" | sort: "order" -%}

<ol>
	{%- for selfacceptancebalancepost in selfacceptancebalanceposts -%}
		<li>
		{{ selfacceptancebalancepost.title }} <span class="tags">In

		{% assign sortedselfacceptancebalancepost = selfacceptancebalancepost.tags | sort_natural  %}

		{%- capture selfacceptancebalanceposttags -%}
		  {%- for tag in sortedselfacceptancebalancepost -%}
		  , <span class="tagmoji">{{ site.data.tagmoji[tag] }}</span>&nbsp;<a href="/{{ selfacceptancebalancepost.categories[0] }}/all/#{{ tag }}">{{ tag | capitalize }}</a>
		  {%- endfor -%}
		{%- endcapture -%}

		{{ selfacceptancebalanceposttags | remove_first: ", " }}.</span>
		</li>
	{%- endfor -%}
</ol>

<h2>Pain</h2>

{%- assign selfacceptancepainposts = site.posts | where: "selfacceptancepain", "true" | sort: "order" -%}

<ol>
	{%- for selfacceptancepainpost in selfacceptancepainposts -%}
		<li>
		{{ selfacceptancepainpost.title }} <span class="tags">In

		{% assign sortedselfacceptancepainpost = selfacceptancepainpost.tags | sort_natural  %}

		{%- capture selfacceptancepainposttags -%}
		  {%- for tag in sortedselfacceptancepainpost -%}
		  , <span class="tagmoji">{{ site.data.tagmoji[tag] }}</span>&nbsp;<a href="/{{ selfacceptancepainpost.categories[0] }}/all/#{{ tag }}">{{ tag | capitalize }}</a>
		  {%- endfor -%}
		{%- endcapture -%}

		{{ selfacceptancepainposttags | remove_first: ", " }}.</span>
		</li>
	{%- endfor -%}
</ol>

<h2>Acceptance</h2>

{%- assign selfacceptanceposts = site.posts | where: "selfacceptance", "true" | sort: "order" -%}

<ol>
	{%- for selfacceptancepost in selfacceptanceposts -%}
		<li>
		{{ selfacceptancepost.title }} <span class="tags">In

		{% assign sortedselfacceptancepost = selfacceptancepost.tags | sort_natural  %}

		{%- capture selfacceptanceposttags -%}
		  {%- for tag in sortedselfacceptancepost -%}
		  , <span class="tagmoji">{{ site.data.tagmoji[tag] }}</span>&nbsp;<a href="/{{ selfacceptancepost.categories[0] }}/all/#{{ tag }}">{{ tag | capitalize }}</a>
		  {%- endfor -%}
		{%- endcapture -%}

		{{ selfacceptanceposttags | remove_first: ", " }}.</span>
		</li>
	{%- endfor -%}
</ol>
