---
layout: page
---
{% include JB/setup %}

<div class="hero-unit">

<div class="row-fluid">
    <div class="span5">    
	  <h2 class="text-left">The open source, <em>affordable</em>, Android based rover</h2>
	  <br>
	  <p>For under $300, you can build your own video streaming robot!</p>
	</div>
    <div class="span4">
	  <object width="560" height="315"><param name="movie" value="//www.youtube.com/v/w5IfFvbPZ24?hl=en_US&amp;version=3"></param><param name="allowFullScreen" value="true"></param><param name="allowscriptaccess" value="always"></param><embed src="//www.youtube.com/v/w5IfFvbPZ24?hl=en_US&amp;version=3" type="application/x-shockwave-flash" width="560" height="315" allowscriptaccess="always" allowfullscreen="true"></embed></object>
    </div>
</div>

</div>

##Latest Posts
{% for post in site.posts limit:3 %}

<div class="alert alert-disabled">
	<a class="close" href="#">{{ post.date | date: "%b %e, %Y"}}</a>
	<h3 class="alert-heading"><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a> <small>in {{post.categories}}</small></h3>
	<p>{{ post.content | strip_html | truncatewords:125}}</p>
	<hr class="thin">
	<div class="alert-actions">
	<span class="tag_box">{% for tag in post.tags %} <a href="{{ BASE_PATH }}{{ site.JB.tags_path }}#{{ tag }}-ref">{{ tag }}</a> {% endfor %}</span>
	<a class="btn btn-info btn-mini" style="float: right;" href="{{ BASE_PATH }}{{ post.url }}">Read More</a>
	</div>
</div>
{% endfor %}


