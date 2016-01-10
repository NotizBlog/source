---
layout:  default
title:   "Grundlagen"
tags:    "Audiophile,Grundlagen,"
---
### Grundlagen.


<div class="row row-offcanvas row-offcanvas-right">
	<div class="col-xs-12 col-sm-9">
		<div class="jumbotron">
			<h1>Hello, world!</h1>
			<p>This is an example to show the potential of an offcanvas layout pattern in Bootstrap. Try some responsive-range viewport sizes to see it in action.</p>
		</div>
		<div class="row">
			{% for post in site.posts %}
			    {% if post.categories contains 'Grundlagen' %}
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
			<a href="#" class="list-group-item active">Link</a>
			<a href="#" class="list-group-item">Link</a>
			<a href="#" class="list-group-item">Link</a>
			<a href="#" class="list-group-item">Link</a>
			<a href="#" class="list-group-item">Link</a>
		</div>
	</div><!--/.sidebar-offcanvas-->
</div><!--/row-->


<ul class="post-list">
    {% for post in site.posts %}
	    {% if post.blog contains 'Audiophil-Grundlagen' %}
			<li>
				<span class="blog-post-meta=">{{ post.date | date: "%b %-d, %Y" }}</span>
				<h3><a cclass="blog-post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
				{{ post.excerpt }}
			</li>
	    {% endif %}
    {% endfor %}
  </ul>