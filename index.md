---
layout: archive
permalink: /
title: "Welcome to the SIPN South website!"
---

<img src="/sipn-south.github.io/images/seaice.png" alt="Sea ice"  width="40%"> 

The Sea ice Prediction Network South (SIPN South) aims to collect, compile and evaluate sea ice forecasts in the Southern Ocean on a real-time basis.

<img src="/sipn-south.github.io/images/Logo2.png" height="25%" width="25%"> 

<div class="tiles">
{% for post in site.posts %}
	{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
