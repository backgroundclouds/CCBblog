---
title: Film Production
layout: landing
description: 'Film Shit'
image: assets/images/pic07.jpg
nav-menu: true
show_tile: true
---

{% assign rank1_post = site.posts | where: "slug", site.data.top_film_posts[0].slug | first %}
{% assign rank2_post = site.posts | where: "slug", site.data.top_film_posts[1].slug | first %}
{% assign rank3_post = site.posts | where: "slug", site.data.top_film_posts[2].slug | first %}
{% assign rank4_post = site.posts | where: "slug", site.data.top_film_posts[3].slug | first %}
{% assign rank5_post = site.posts | where: "slug", site.data.top_film_posts[4].slug | first %}



<div id="main">
    <!-- Other sections of your landing page -->

<section id="one">
    <div class="inner">
        {% if rank1_post %}
            <header class="major">
                <h2>Featured Post</h2>
                    <h3><a href="{{ rank1_post.url | prepend: site.baseurl }}">{{ rank1_post.title }}</a></h3>
				<article>
                <p>{{ rank1_post.description }}</p>
                <ul class="actions">
                    <li><a href="{{ rank1_post.url | prepend: site.baseurl }}" class="button">Read More</a></li>
                </ul>
            </article>
        {% else %}
            <p>Featured post not found.</p>
        {% endif %}
	</header>


<!-- Two -->
<section id="two" class="spotlights">
    <section>
        <a href="{{ rank2_post.url | prepend: site.baseurl }}" class="image">
            <img src="{{ '/assets/images/pic08.jpg' | prepend: site.baseurl }}" alt="" data-position="center center" />
        </a>
        <div class="content">
            <div class="inner">
                <header class="major">
                    <h3> <a href="{{ rank2_post.url | prepend: site.baseurl }}"> {{ rank2_post.title }}</a>
					</h3>
                </header>
                <p>{{ rank2_post.description }}</p>
                <ul class="actions">
                    <li><a href="{{ rank2_post.url | prepend: site.baseurl }}" class="button">More</a></li>
                </ul>
            </div>
        </div>
    </section>
    <section>
        <a href="{{ rank3_post.url | prepend: site.baseurl }}" class="image">
            <img src="{{ '/assets/images/pic09.jpg' | prepend: site.baseurl }}" alt="" data-position="25% 25%" />
        </a>
        <div class="content">
            <div class="inner">
                <header class="major">
                    <h3><a href="{{ rank3_post.url | prepend: site.baseurl }}"> {{ rank3_post.title }}</a>
					</h3>
                </header>
                <p>{{ rank3_post.description }}</p>
                <ul class="actions">
                    <li><a href="{{ rank3_post.url | prepend: site.baseurl }}" class="button"> More</a></li>
                </ul>
            </div>
        </div>
    </section>
	<br><br>
</section>




<!-- Three -->
<section id="three" class="spotlights">
	<div class="inner">
		<header class="major">
			<h3>All Production Posts</h3>
		<p> For a text block list of all brand posts go here<br><br>
		<ul class="actions">
			<li><a href="generic.html" class="button next">Here</a></li>


