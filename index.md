---
layout: default
title: Hyperspace by HTML5 UP
---

<!-- Wrapper -->
<div id="wrapper">

<!-- Intro -->
<section id="intro" class="wrapper style1 fullscreen fade-up">
	<div class="inner">
		<h1>Jason is trying to grow up...</h1>
		<p> But he spends his time learning and building new things instead.</p>
		<ul class="actions">
			<li><a href="#one" class="button scrolly">Find out what Jason is up to</a></li>
		</ul>
	</div>
</section>

<section id="one" class="wrapper style2 fade-up spotlights">
	<section>
		<div class="content">
			<div class="inner">
				<h2>About Jason</h2>
				<div>
					<p>I'm a design-minded, detail oriented product manager with software engineering qualities. I'm passionate about combining beautiful code with beautiful design while creating a product that people can truly love.</p>
					<p>I have experience managing products from idea to launch professionally and have been developing and designing software for the web, from single page web application to progressive microservice servers. I strive to create products that not only functions efficiently under the hood, but also can be enjoyed by all.</p>
					<br>
				</div>
			</div>
		</div>
	<div class="content">
		<div class="inner">
			<img style="border-radius:50%" alt="" data-position="center center" src="{{site.profilepicture}}" />
		</div>
	</div>
	</section>
</section>

<section id="two" class="wrapper style3 fade-up">
	<div class="inner">
		<h2>TL:DR Jason's Curriculum Vitae</h2>
		<div class="features">
			<section>
				<span class="icon major fa-graduation-cap"></span>
				<h3>Education</h3>
				<p>Graduated from UCLA in 2010 with an Economics major and minors in both Urban Planning and Regional Studies. </p>
				<p>Graduated from Hack Reactor in 2017 focused on Software Engineering with leading industry techstack.</p>
			</section>
			<section>
				<span class="icon major fa-briefcase"></span>
				<h3>Work Experience</h3>
				<p>BI Manager @ Lifefactory (≈4 years) <br>
				Co-founder @ Ludociti (≈1 year) <br>
				Analyst @ General Electric Aviation (≈1 year) <br>
				FP&A Intern @ AXA Advisors (≈3 months) <br>
				Management Intern @ Aflac (≈3 months)
				</p>
			</section>
			<section>
				<span class="icon major fa-cog"></span>
				<h3>Product Management Experience</h3>
				<p>Netsuite ERP implementation @ Lifefactory <br>
				Lifefactory Liquids iOS Mobile App @ Lifefactory <br>
				Punchfunder Alpha Stage @ Ludociti</p>
			</section>
			<section>
				<span class="icon major fa-desktop"></span>
				<h3>Software Engineering Experience</h3>
				<p>Eventscore iOS Mobile App @ Hack Reactor <br>
				Hella Amazing Race App @ Hack Reactor <br>
				Get Quoted App @ Hack Reactor
				</p>
			</section>
			<section>
				<span class="icon major fa-code-fork"></span>
				<h3>Product Management Skills</h3>
				<p>
				<b>Applications:</b> Microsoft Office Suite, Balsamiq <br>
				<b>Data Analysis Tools:</b> Qlik, Netsuite Analytics, Tableau, MicroStrategy <br>
				<b>Productivity Tools:</b> Git, Trello, Basecamp <br>
				<b>Languages:</b> Mandarin Chinese
				</p>
			</section>
			<section>
				<span class="icon major fa-code"></span>
				<h3>Technical Skills</h3>
				<p>
					<b>Frameworks/Libraries:</b> React/React Native, Angular.js, Express, HTML, CSS/SCSS, Flexbox, Material UI, jQuery, Redux, Jekyll, Webpack, Babel, Heroku, AWS, bCrypt, Crypto, Docker <br>
					<b>Software Engineering:</b> Test driven development (units/smoke/integration), architecture design, code review, agile dev <br>
					<b>Technical Languages:</b> JavaScript, JSX, SQL, EDI, Visual Basic.Net, Ruby, Python
				</p>
			</section>
		</div>
		<p><em>Approximate proficiency in descending order from left to right</em></p>		
		<ul class="actions">
			<li><a href="{{site.baseurl}}download/JasonKuoCV.pdf" class="button">Check out Jason's Current Resume in PDF</a></li>
		</ul>
	</div>
</section>

<section id="three" class="wrapper style1 spotlights">
	{% for project in site.projects limit:3 %}
		<section>
			<img src="images/pic01.jpg" class="image" alt="" data-position="center center" />
			<div class="content">
				<div class="inner">
					<h2>{{project.title}}</h2>
					<p>{{project.description}}</p>
					<p>Tech Stack: {{project.techstack}}</p>
					<ul class="actions">
						<li><a href="{{site.baseurl}}projects/{{project.filename}}" class="button">Learn more</a></li>
					</ul>
				</div>
			</div>			
		</section>
	{% endfor %}
</section>

<section id="four" class="wrapper style1 fade-up">
	<div class="inner">
		<h2>Get in touch</h2>
		<p>I'm always interesting in learning more about others and open to any feedback. Feel free to drop a message. Promise, I don't <em>"byte"</em>.</p>
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
