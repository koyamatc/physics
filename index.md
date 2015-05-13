---
title: physics
layout: default
---

#Physics

- - -

__Khan Academy__ で勉強したことのまとめです
===

###index

<div class="row">
	<div class="col-sm-4">
		<h3><span class="label label-info">One Dimensional Motion</span></h3>
		<ol class="post-list">
 			{% for post in site.categories.oned-motion %}
   				<li><a href="{{ post.url }}">{{ post.postTitle }}</a></li>
 			{% endfor %}
		</ol>			
		<h3><span class="label label-info">Two Dimensional Motion</span></h3>
		<ol class="post-list">
 			{% for post in site.categories.twod-motion %}
   				<li><a href="{{ post.url }}">{{ post.postTitle }}</a></li>
 			{% endfor %}
		</ol>			
	</div>
	<div class="col-sm-4">
		<h3>
			<span class="label label-info">Forces and Newton's laws of motion
			</span>
		</h3>
		<h3>
			<span class="label label-default">
				Newton's laws of motion
			</span>
		</h3>
		<ol class="post-list">
 			{% for post in site.categories.newton-laws-motion %}
   				<li><a href="{{ post.url }}">{{ post.postTitle }}</a></li>
 			{% endfor %}
		</ol>			
	</div>


</div>