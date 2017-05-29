---
layout: default
title: Hyperspace by HTML5 UP
---

<!-- Sidebar -->
{% include sidebar.html %}

<!-- Wrapper -->
<div id="wrapper">

<!-- Intro -->
<section id="intro" class="wrapper style1 fullscreen fade-up">
	<div class="inner">
		<h1>Jason is trying to grow up...</h1>
		<p> But he spends his time learning and building new things.</p>
		<ul class="actions">
			<li><a href="#one" class="button scrolly">Learn more</a></li>
		</ul>
	</div>
</section>

<!-- One -->
<section id="one" class="wrapper style2 spotlights">
	<section>
		<a href="#" class="image"><img src="images/pic01.jpg" alt="" data-position="center center" /></a>
		<div class="content">
			<div class="inner">
				<h2>Sed ipsum dolor</h2>
				<p>Phasellus convallis elit id ullamcorper pulvinar. Duis aliquam turpis mauris, eu ultricies erat malesuada quis. Aliquam dapibus.</p>
				<ul class="actions">
					<li><a href="#" class="button">Learn more</a></li>
				</ul>
			</div>
		</div>
	</section>
	<section>
		<a href="#" class="image"><img src="images/pic02.jpg" alt="" data-position="top center" /></a>
		<div class="content">
			<div class="inner">
				<h2>Feugiat consequat</h2>
				<p>Phasellus convallis elit id ullamcorper pulvinar. Duis aliquam turpis mauris, eu ultricies erat malesuada quis. Aliquam dapibus.</p>
				<ul class="actions">
					<li><a href="#" class="button">Learn more</a></li>
				</ul>
			</div>
		</div>
	</section>
	<section>
		<a href="#" class="image"><img src="images/pic03.jpg" alt="" data-position="25% 25%" /></a>
		<div class="content">
			<div class="inner">
				<h2>Ultricies aliquam</h2>
				<p>Phasellus convallis elit id ullamcorper pulvinar. Duis aliquam turpis mauris, eu ultricies erat malesuada quis. Aliquam dapibus.</p>
				<ul class="actions">
					<li><a href="#" class="button">Learn more</a></li>
				</ul>
			</div>
		</div>
	</section>
</section>

<!-- Two -->
<section id="two" class="wrapper style3 fade-up">
	<div class="inner">
		<h2>What we do</h2>
		<p>Phasellus convallis elit id ullamcorper pulvinar. Duis aliquam turpis mauris, eu ultricies erat malesuada quis. Aliquam dapibus, lacus eget hendrerit bibendum, urna est aliquam sem, sit amet imperdiet est velit quis lorem.</p>
		<div class="features">
			<section>
				<span class="icon major fa-code"></span>
				<h3>Lorem ipsum amet</h3>
				<p>Phasellus convallis elit id ullam corper amet et pulvinar. Duis aliquam turpis mauris, sed ultricies erat dapibus.</p>
			</section>
			<section>
				<span class="icon major fa-lock"></span>
				<h3>Aliquam sed nullam</h3>
				<p>Phasellus convallis elit id ullam corper amet et pulvinar. Duis aliquam turpis mauris, sed ultricies erat dapibus.</p>
			</section>
			<section>
				<span class="icon major fa-cog"></span>
				<h3>Sed erat ullam corper</h3>
				<p>Phasellus convallis elit id ullam corper amet et pulvinar. Duis aliquam turpis mauris, sed ultricies erat dapibus.</p>
			</section>
			<section>
				<span class="icon major fa-desktop"></span>
				<h3>Veroeros quis lorem</h3>
				<p>Phasellus convallis elit id ullam corper amet et pulvinar. Duis aliquam turpis mauris, sed ultricies erat dapibus.</p>
			</section>
			<section>
				<span class="icon major fa-chain"></span>
				<h3>Urna quis bibendum</h3>
				<p>Phasellus convallis elit id ullam corper amet et pulvinar. Duis aliquam turpis mauris, sed ultricies erat dapibus.</p>
			</section>
			<section>
				<span class="icon major fa-diamond"></span>
				<h3>Aliquam urna dapibus</h3>
				<p>Phasellus convallis elit id ullam corper amet et pulvinar. Duis aliquam turpis mauris, sed ultricies erat dapibus.</p>
			</section>
		</div>
		<ul class="actions">
			<li><a href="#" class="button">Learn more</a></li>
		</ul>
	</div>
</section>

<!-- Three -->
<section id="three" class="wrapper style1 fade-up">
	<div class="inner">
		<h2>Get in touch</h2>
		<p>I'm always interesting in learning more about others and thoughts. Feel free to drop a message. Promise, I don't <em>"byte"</em>.</p>
		<div class="split style1">
			<section>
				<form method="post" action="https://formspree.io/{{site.email}}">
					<div class="field half first">
						<label for="name">Name</label>
						<input type="text" name="name" id="name" />
					</div>
					<div class="field half">
						<label for="email">Email</label>
						<input type="text" name="_replyto" id="email" />
					</div>
					<div class="field">
						<label for="message">Message</label>
						<textarea name="message" id="message" rows="5"></textarea>
					</div>
					<ul class="actions">
					<li>
						<input type="submit" value="Send Message">
					</li>
					</ul>
				</form>
			</section>
			<section>
				<ul class="contact">
					<li>
						<h3>Email</h3>
						<a href="#">{{ site.email }}</a>
					</li>
					<li>
						<h3>Phone</h3>
						<span>{{ site.phone }}</span>
					</li>
					<li>
						<h3>Social</h3>
						<ul class="icons">
						{% if site.github_username %}
							<li>
								<a href="{{ site.github_url }}">
									<i class="fa fa-github icon"></i> <span> {{ site.github_username }} </span>
								</a>
							</li>
						{% endif %}
						{% if site.linkedin_username %}
							<li>
								<a href="{{ site.linkedin_url }}">
									<i class="fa fa-linkedin"></i> <span> {{ site.linkedin_username }} </span>
								</a>
							</li>
						{% endif %}
						{% if site.facebook_username %}
							<li>
								<a href="{{ site.facebook_url }}">
									<i class="fa fa-facebook"></i> <span> {{ site.facebook_username }} </span>
								</a>
							</li>
						{% endif %}
						{% if site.twitter_username %}
							<li>
								<a href="{{ site.twitter_url }}">
									<i class="fa fa-twitter"></i> <span> {{ site.twitter_username }} </span>
								</a>
							</li>
						{% endif %}
						{% if site.instagram_username %}
							<li>
								<a href="{{ site.instagram_url }}">
									<i class="fa fa-instagram"></i> <span> {{ site.instagram_username }} </span>
								</a>
							</li>
						{% endif %}
						</ul>
					</li>
				</ul>
			</section>
		</div>
	</div>
</section>
