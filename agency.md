---
title: Agency
layout: landing
# description: 'Creative Darlings'
sub_description: |
    Experiments have shown that notions of causality and agency
    are **intimately** related —K. Cukier
image: assets/images/pic07.jpg
nav-menu: true
show_tile: true
landing-description:
---
{% assign rank1_post = site.posts | where: "slug", site.data.top_agency_posts[0].slug | first %}
{% assign rank2_post = site.posts | where: "slug", site.data.top_agency_posts[1].slug | first %}
{% assign rank3_post = site.posts | where: "slug", site.data.top_agency_posts[2].slug | first %}
{% assign rank4_post = site.posts | where: "slug", site.data.top_agency_posts[3].slug | first %}
{% assign rank5_post = site.posts | where: "slug", site.data.top_agency_posts[4].slug | first %}





<div id="main">
    <!-- Other sections of your landing page -->

<section id="featured-post">
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
            <h3> All empty. Come back later.</h3>
            <br>
        {% endif %}
	<!-- </header> -->



<!-- Two -->
<section id="two" class="spotlights">
{% if rank2_post.title %}
    <section>
        <a href="{{ rank2_post.url | prepend: site.baseurl }}" class="image">
            <img src="{{ '/assets/images/pic08.jpg' | prepend: site.baseurl }}" alt="" data-position="center center" />
        </a>
        <div class="content">
            <div class="inner">
                <header class="major">
                    <h3>{{ rank2_post.title }}</h3>
                </header>
                <p>{{ rank2_post.description }}</p>
                <ul class="actions">
                    <li><a href="{{ rank2_post.url | prepend: site.baseurl }}" class="button">More</a></li>
                </ul>
            </div>
        </div>
    </section>
    {% endif %}
    {% if rank3_post.title %}
    <section>
        <a href="{{ rank3_post.url | prepend: site.baseurl }}" class="image">
            <img src="{{ '/assets/images/pic09.jpg' | prepend: site.baseurl }}" alt="" data-position="25% 25%" />
        </a>
        <div class="content">
            <div class="inner">
                <header class="major">
                    <h3>{{ rank3_post.title }}</h3>
                </header>
                <p>{{ rank3_post.description}}</p>
                <ul class="actions">
                    <li><a href="{{ rank3_post.url | prepend: site.baseurl }}" class="button"> More</a></li>
                </ul>
            </div>
        </div>
    </section>
    {% endif %}
		<br><br>
</section>

<!-- Three -->
<!-- Turn this on later, after settign up Al Brand Posts page -->
<!-- <section id="three" class="spotlights">
	<div class="inner">
		<header class="major">
			<h3>All Brand Posts</h3>
		<p> For a text block list of all brand posts go here<br><br>
		<ul class="actions">
			<li><a href="generic.html" class="button next">Here</a></li> -->


