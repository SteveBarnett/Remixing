---
layout: page
title: Self-compassion
longerform: true
added: 2023-08-13
updated: 2023-08-13
---

{%- assign selfcompassionposts = site.posts | where: "selfcompassion", "true" | sort: "order" -%}

<ol>
	<li>For behaviour, there's the expected, the observed, and the interpreted.
		<ul>
		  	<li>The expected, the "should", is set lower than you think. Allow for perfectionism and people-pleasing tendencies.</li>
		 	<li>The Inner Critic's interpretation is set much lower than the observed.</li>
	 	</ul>
	</li>
	{%- for selfcompassionpost in selfcompassionposts -%}
		<li>
		{{ selfcompassionpost.title }} <span class="tags">In

		{% assign sortedselfcompassionpost = selfcompassionpost.tags | sort_natural  %}

		{%- capture selfcompassionposttags -%}
		  {%- for tag in sortedselfcompassionpost -%}
		  , <span class="tagmoji">{{ site.data.tagmoji[tag] }}</span>&nbsp;<a href="/{{ selfcompassionpost.categories[0] }}/all/#{{ tag }}">{{ tag | capitalize }}</a>
		  {%- endfor -%}
		{%- endcapture -%}

		{{ selfcompassionposttags | remove_first: ", " }}.</span>
		</li>
	{%- endfor -%}
</ol>
