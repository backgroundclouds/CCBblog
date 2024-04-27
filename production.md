---
title: Production
layout: landing
position: 3
# description: 'And other shit'
sub_description: |
    
    Turn these **goons** into **goombas** in under an hour'
    
image: assets/images/pic07.jpg
nav-menu: true
show_tile: true
---
{% assign rank1_post = site.posts | where: "title", site.data.top_film_posts[0].title | first %}
{% assign posts_array = site.data.top_film_posts | slice: 1, site.data.top_brand_posts.size %}

<style>
  #category-spotlights-wrapper {
    max-width: 1200px; /* Adjust this to fit your design */
    margin: 0 auto; /* Centers the section on the page */
    padding: 50px; /* Adds padding around the content */
    background-color: #393b54; /* Light background for the section */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Soft shadow for depth */
    border-radius: 8px; /* Optional: rounds corners */
  }
  
  #category-spotlights-wrapper img {
    width: auto;
    max-width: 350px; /* Adjust the width as needed */
    height: auto;
    display: block;
    margin: 10px auto; /* Centers image */
    border-radius: 8px; /* Rounds corners of images */
  }
</style>



<div id="main">
    <!-- Other sections of your landing page -->



<section id="featured-post">
    <div class="inner">
        {% if rank1_post %}
            <header class="major">
                <h2>Featured Post</h2>
                    <h3><a href="{{ rank1_post.url | prepend: site.baseurl }}">{{ rank1_post.title }}</a></h3>
				</header>
                <p>{{ rank1_post.description }}</p>
                <ul class="actions">
                    <li><a href="{{ rank1_post.url | prepend: site.baseurl }}" class="button">Read More</a></li>
                </ul>
        {% else %}
            <h3> All empty. Come back later.</h3>
            <br>
        {% endif %}
        </div>
        </section>
	<!-- </header> -->




  <!-- Spotlights Section -->
<section id="two" class="spotlights">
        <div id="category-spotlights-wrapper">
            {% for post_entry in posts_array %}
                {% assign current_post = site.posts | where: "title", post_entry.title | first %}
                {% if current_post %}
                    <section>
                        <header>
                            <h3><a href="{{ current_post.url | prepend: site.baseurl }}">{{ current_post.title }}</a></h3>
                        </header>
                        <a href="{{ current_post.url | prepend: site.baseurl }}" class="image">
                            <img src="{{ current_post.image | prepend: site.baseurl }}" alt="{{ current_post.title }}" data-position="center center" />
                        </a>
                        <div class="content">
                            <p>{{ current_post.description }}</p>
                            <ul class="actions">
                                <li><a href="{{ current_post.url | prepend: site.baseurl }}" class="button">More</a></li>
                            </ul>
                        </div>
                    </section>
                {% endif %}
            {% endfor %}
        </div>
    </section>
</div>



<!-- Make this visible later when I have more than 5 posts -->

<!-- Three
<section id="three" class="spotlights">
	<div class="inner">
		<header class="major">
			<h3>All Production Posts</h3>
		<p> For a text block list of all brand posts go here<br><br>
		<ul class="actions">
			<li><a href="generic.html" class="button next">Here</a></li>
 -->


