---
layout: page
title:  Hella Amazing Race
date:   0003-01-01
filename: hellaamazingrace
techstack: MongoDb, Express, React, Node.js
webtechnologies: React Router, Bluebird, Google Maps, Pubnub, WebRTC, Material UI
api: Google Maps, Google Cloudvision, Google Places, Facebook
description: Real-time social racing application with photo recognition.
support: [jquery, gallery]
galleryid: hellaamazingrace
mainphoto: hellaamazingrace-main.png
sourcecode: https://github.com/Quoted/HellaAmazingRace
---
<!-- style="object-fit: none; object-position: 50% 50%; position: absolute; background: rgba(0, 0, 0, .5); min-width: 100%; height: auto" -->
<!-- Intro -->
<section id="intro" class="wrapper style1 fade-up">
	<div class="inner">
		<h1>{{page.title}}</h1>
		<p>{{page.description}}</p>
		<ul class="actions">
			<li><a href="#" class="button disabled" >Demo</a></li>
      <li><a href="#" class="button">Source Code</a></li>
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
            What's better than the Amazing Race - a Hella Amazing Race. Hella Amazing Race is our interpretation of how races should be conducted in unfamiliar parts of town; Races should include content awareness for it's path and surroundings.
          </p>
					<p>
            Our app allows users to create races by picking specific destinations by checkpoints utilizing Google Places and allows users to compete amongst themselves real-time. In order to make things interesting, the application requires the racers two forms of checkpoint validations: <br>
            <ol>
              <li>Geolocation vicinity from destinations</li>
              <li>Photo Recognition based on desired input</li>
            </ol>
            Through the use of Google Cloudvision and Places, the application randomly chooses a point of interest or object for the racers to take a picture for photo validation.
          </p>
          <p>
            <b>Tech Stack:</b> {{page.techstack}} <br>
            <b>Web Technologies:</b> {{page.webtechnologies}} <br>
            <b>Api:</b> {{page.api}}
          </p>
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
		<h2>The Concept</h2>
    <h3>Goal</h3>
    <p>As a legacy project, we decided to enhance the current code based to accept multiple racers and make checkpoints more meaning by incorporating objectives.</p>
		<div class="features">
      <section>
				<span class="icon major fa-user"></span>
				<h3>User Cases</h3>
				<ul>
          <li>I expect to be able to create races and start races.</li>
          <li>I expect to be able to race against other users simultaneously.</li>
          <li>I expect to be able race using my cellphone.</li>
          <li>I expect to be able to take pictures of objectives and get some sort of validation that the objective has been met.</li>
        </ul>
			</section>
			<section>
				<span class="icon major fa-code"></span>
				<h3>System Requirements</h3>
				<ul>
          <li>Port pre-existing code to mobile by making it responsive to device's screen size via material ui components</li>
          <li>Pass image blob to server for further image analysis by Google Cloudvision</li>
          <li>Increase the number of subscribers for each race event via Pubnub</li>
				</ul>
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
        You'll always run into unexpected problems with any legacy project. For one, the legacy code did not enable multiple users to join a race. Another example was the fact that the legacy code was built to be a web app with no responsive designs to scale to mobile resolutions. However, the one that takes the cake, that is still left incomplete for this project, is the storage of cached data.<br>
        <br>
        The application handled states locally for all components which became problematic whenever views were switched during a race to access the checkpoint component. Without the incorporation of Redux or storing all functions in its root container, it became impossible to complete the project.<br>
        <br>
        All in all, it was a good experience to development and touch base on new technologies that I've never encountered (i.e, Google Cloudvision and WebRTC)<br>
      </div>
    </div>
  </div>
  <div class="content">
    <div class="inner">
    {% highlight javascript %}
    {% endhighlight %}
    </div>
  </div>
</section>
</section>
