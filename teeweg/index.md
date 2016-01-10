---
layout:  default
title:   "Teeweg"
excerpt: "Rund um die Oolong Tee Welt."
---

# Oolong Tee.
<div class="row row-offcanvas row-offcanvas-right">
	<div class="col-xs-12 col-sm-9">
		<div class="jumbotron">
			<h1>Hello, world!</h1>
			<p>This is an example to show the potential of an offcanvas layout pattern in Bootstrap. Try some responsive-range viewport sizes to see it in action.</p>
		</div>
		<div class="row">
			{% for post in site.posts %}
			    {% if post.categories contains 'teeweg' %}
				    <div class="col-xs-6 col-lg-4">
						<h3><a class="blog-post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></br><span class="blog-post-meta=">{{ post.date | date: "%b %-d, %Y" }}</span></h3>
						<p>{{ post.excerpt }}</p>
						<p><a class="btn btn-default" href="{{ post.url | prepend: site.baseurl }}" role="button">Lesen &raquo;</a></p>
					</div>
			    {% endif %}
			{% endfor %}
		</div><!--/row-->
	</div><!--/.col-xs-12.col-sm-9-->


	<div class="col-xs-6 col-sm-3 sidebar-offcanvas" id="sidebar">
		<div class="list-group">
			<a href="#allposts" class="list-group-item">Alle Inhalte</a>
			{% for category in site.categories.cat %}
			<a href="#{{ category | first | remove:' ' }}" class="list-group-item">{{ category | first }}</a> {% if forloop.last %}{% else %}{% endif %}
			{% endfor %}
		</div>
	</div><!--/.sidebar-offcanvas-->
</div><!--/row-->



<!--/ All Posts %}-->
<div class="catbloc" id="allposts">
	<h2>Alle Inhalte</h2>
	<ul>
		{% for post in site.posts %}
		{% if post.categories contains 'teeweg' %}
		<li>
			<a href="{{ post.url }}">
			<time>{{ post.date | date: "%-d %B %Y" }}</time>
			{{ post.title }}
			</a>
		</li>
		{% endif %}
		{% endfor %}
	</ul>
</div>

<!--/ Posts by Categories %}-->
<div>
{% for category in site.categories %}
{% if post.categories contains 'teeweg' %}
	<div class="catbloc" id="{{ category | first | remove:' ' }}">
		<h2>{{ category | first }}</h2>
		<ul>
			{% for posts in category %}
				{% for post in posts %}
					{% if post.url %}
			<li>
				<a href="{{ post.url }}">
				<time>{{ post.date | date: "%-d %B %Y" }}</time>
				{{ post.title }}
				</a>
			</li>
					{% endif %}
				{% endfor %}
			{% endfor %}
		</ul>
	</div>
{% endif %}
{% endfor %}
</div>