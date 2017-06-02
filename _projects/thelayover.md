---
layout: page
title:  The Layover
date:   0001-01-01
filename: thelayover
techstack: MongoDb, Express, React, Node.js
webtechnologies: TBD
api: TBD
description: A stealth project aimed to solve the greatest problem known to travelers' all across the globe - the layover. Stay in touch for more updates on the project.
support: [jquery, gallery]
galleryid: thelayover
mainphoto: thelayover_main.png
sourcecode: #
---

<!-- Intro -->
<section id="intro" class="wrapper style1 fade-up">
  <img style="position: absolute; background: rgba(0, 0, 0, .5); min-width: 100%; height: auto" src="{{site.baseurl}}images/thelayover_main.png"  alt="" data-position="center center" />
	<div class="inner">
		<h1>{{page.title}}</h1>
		<p>{{page.description}}</p>
		<ul class="actions">
			<li><a href="#" class="button disabled" >Demo</a></li>
      <li><a href="{{page.sourcecode}}" class="button disabled">Source Code</a></li>
		</ul>
	</div>
</section>

<section id="one" class="wrapper style2 fade-up spotlights">
	<section>
		<div class="content">
			<div class="inner">
				<h2>About {{page.title}}</h2>
				<div>
					<p>
            TBD
          </p>
          <p>
            <b>Tech Stack:</b> {{page.techstack}} <br>
            <b>Web Technologies:</b> {{page.webtechnologies}} <br>
            <b>Api:</b> {{page.api}}
          </p>
					<br>
				</div>
			</div>
		</div>
    <div class="content">
      <div class="inner">
        {% include gallery.html %}
      </div>
    </div>
	</section>
</section>

<section id="two" class="wrapper style3 fade-up">
	<div class="inner">
		<h2>Key Requirements</h2>
		<div class="features">
			<section>
				<span class="icon major fa-user"></span>
				<h3>User</h3>
				<p>TBD</p>
			</section>
			<section>
				<span class="icon major fa-code"></span>
				<h3>System</h3>
          <p>TBD</p>
			</section>
		</div>
	</div>
</section>

<section id="three" class="wrapper style1 fade-up spotlights">
	<section>
		<div class="content">
			<div class="inner">
				<h2>Technical Challenges</h2>
				<div>
          TBD
				</div>
			</div>
		</div>
	</section>
</section>
