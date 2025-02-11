---
layout: page
title: Self-compassion
ifs: true
added: 2023-08-13
updated: 2025-02-11
---

{%- assign selfcompassionposts = site.posts | where: "selfcompassion", "true" | sort: "order" -%}

<blockquote class="alt"><p>Mind the gap (between target behaviour and actual behaviour).</p></blockquote>

<ol>
	<li>The People-Pleaser frames the target as a requirement for worthiness.</li>
	<li>The Perfectionist moves the target value unrealistically high.</li>
	<li>The Critic moves the actual value lower than it really is.</li>
</ol>

<p>The gap now appears very big.</p>

<ol>
	<li>The People-Pleaser says: not meeting requirements / expectations means you're unworthy.</li>
	<li>The Perfectionist says: the target was the minimum, so this counts as a failure.</li>
	<li>The Critic says: failure deserves punishment.</li>
</ol>

<p>The Perfectionist and The Critic also team up to tilt towards shame (I am bad) and away from guilt (I did bad).</p>

<p><strong>Oof!</strong> 😅</p>

<p>All models are wrong, but some are useful. I was poking around at <a href="https://en.wikipedia.org/wiki/Enneagram_of_Personality">the Enneagram of Personality</a> again the other day, and I've got an <a href="https://ifs-institute.com/">IFS</a> (Internal Family Systems) book (<a href="https://www.goodreads.com/book/show/55384168-no-bad-parts">No Bad Parts</a>) on my reading list. These two together prompted me to update this page.</p>

<p></p>

<h2>Potential roots</h2>

<ul>
	<li>The People-Pleaser perhaps formed as a increase-the-feedback-loop reaction to a model of quiet, subtle, praise.</li>
	<li>The Perfectionist perhaps formed as a bit of a clarity-based complementary-opposite-reaction to a model of quietness and indirectness.</li>
	<li>The Critic is perhaps part of my natural tendency for analysis.</li>
	<li>I have a perhaps <a href="/thinking/traits/">trait</a>-based tendency towards thinking in binaries, so either something is a success or a failure, no middle ground.</li>
</ul>

<h2>Practice approach</h2>

<blockquote class="alt">
	<ul>
		<li>Notice it's a moment of suffering.</li>
		<li>Watch the feeling and the feeling tone arise and pass away.</li>
		<li>Notice the emptiness of the three aspects.</li>
	</ul>
</blockquote>

<p>A riff on RAIN.</p>

<ol>
	<li>Notice the somatic experience associated with the mental experience.</li>
	<li>Watch the somatic experience (arise and) pass away.</li>
	<li>Notice the emptiness of the mental experience.</li>
</ol>

<h3>Conceptual</h3>

<p>You can't make The People-Pleaser, The Perfectionist, and The Critic shut up. But you don't have to listen to them. And the less you listen, the more they quiet down.</p>

<ol>
	<li>What is the gap for? Maybe a figment.</li>
	<li>What is the expected value? Probably lower.</li>
	<li>What is the actual value? Probably higher.</li>
	<li>Compare base to actual, not actual to expected.</li>
	<li>Coach not Critic is better for improvement.</li>
</ol>

<p>And! The three aspects are empty (in the Buddhist sense). They conditionally co-arise. They interact with and change each other. They go around in a circle, reinforcing each other and backing each other up. But digging into them, you can't find anything solid or fixed or really Real.</p>

<h3>Aphorismical (‽)</h3>

<ul>
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
</ul>
