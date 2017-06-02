---
layout: page
title:  Eventscore iOS App
date:   0002-01-01
filename: eventscore
techstack: MongoDb, Express, React Native, Node.js
webtechnologies: React Router Flux, Redux, Cheerio, Bluebird, Google Maps, D3.js, CRON
api: IBM Watson, Shopify, Klout, Songkick
description: A concert discovery application using predictive and public social influence analysis powered by React Native, Redux, and much more.
support: [jquery, gallery]
galleryid: eventscore
mainphoto: eventscore-eventlist-0001-750x1334.png
sourcecode: https://github.com/Eventscore
---

<!-- Intro -->
<section id="intro" class="wrapper style1 fade-up">
  <img style="position: absolute; background: rgba(0, 0, 0, .5); min-width: 100%; height: auto" src="{{site.baseurl}}images/eventscore_main.jpg"  alt="" data-position="center center" />
	<div class="inner">
		<h1>{{page.title}}</h1>
		<p>{{page.description}}</p>
		<ul class="actions">
			<li><a href="#" class="button disabled" >Demo</a></li>
      <li><a href="{{page.sourcecode}}" class="button">Source Code</a></li>
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
            As self-proclaimed music gurus, we decided that discovering new music is best when heard live. After countless of hours scrambling around and pitching ideas left-to-right, we ended up with Eventscore - A concert discovering tool built based on geolocation and social perception.
          </p>
					<p>
            Our app curates a list of upcoming concerts given your search query and scores the event based on an algorithm that concatenates various scores from 3rd Party API services (Spotify, Klout, SeatGeek, and etc) as well as social tones from social media sources to one. The application utilizes microservices to serve fetched social tones for each particular event based on a timed job schedule.
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
				<ul>
          <li>I expect to get reliable and bare minimum information in regards to upcoming events (Artist, Location, Datetime, Scores).</li>
          <li>I expect to be able to filter events by keywords and locations.</li>
          <li>I expect to be able to buy tickets seamlessly through the application.</li>
          <li>I expect multiple scores regarding the event representing their respective categories.</li>
        </ul>
			</section>
			<section>
				<span class="icon major fa-code"></span>
				<h3>System</h3>
				<ul>
          <li>I expect all routes to be accessible and working expectingly using React Router Flux.</li>
          <li>I expect Redux to store all reducers and states</li>
          <li>I expect the microserver bot to crawl through various websites and capture nodes that pertains to the concerts in our database.</li>
          <li>I expect all processes to asynchronous activity to be handled in a systematic way ensuring point-to-point connection.</li>
          <li>I expect IBM Watson tone analyzer to determine social perception of the nodes captured.</li>
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
          There were a myriad of issues with this project altogether.
          <br>
          <ul>
            <li>Where to pull the appropriate sources to get ticket sales information?</li>
            <li> Where to forecast sales from resellers and how to appropriately determine demand from those sales</li>
            <li>Which algorithm would best represent the score calculation of these various concerts and what external factors would need to be accounted for?</li>
            <li>What kind of techstack and system architecture is most fitting for the application?</li>
          </ul>
          Nevertheless, as a collective group, we decided that finishing the key requirements mentioned above as a MVP would be most critical and ended up curating data from reputable 3rd party APIs while basing the algorithm on a weighted logarithmic scale to ensure that keywords with many social mentions can still produce a positive result. Through proper coordination, our team of 4 finished the entire ideation and full-stack development within 4 weeks. <br>
          <br>
          In regards to development, the greatest technical would most likely be the sheer amount of Promises used - I call them the promises from hell. To the right, you'll see a piece code I've written for the bot to crawl through various websites. In short, there are nested promises within promises with more promises within helper functions. On top of that, this segment doesn't even tap into tone analysis or data aggregated which leads to more promises.<br>
          <br>
          Let's just say I've gotten pretty good at keeping my promises.
				</div>
			</div>
		</div>
    <div class="content">
      <div class="inner">
      {% highlight javascript %}
        exports.initiateCrawl = function() {
          return Promise.all(sites.map((site) => {
            return new Promise((resolve, reject) => {
              var SEARCH_WORD = {};
              Index.keywords.forEach( (keyword) => {
                SEARCH_WORD[keyword] = [];
              });
              site = 'https://' + site;
              url = new URL(site);
              baseUrl = url.protocol + '//' + url.hostname;
              SEARCH_WORD.hostname = url.hostname;
              request(url.origin, function(error, response, body) {
                if(response.statusCode !== 200) {
                  reject(error);
                }
                var $ = cheerio.load(body, {ignoreWhitespace: true});
                var htmlBody = $('html > body');
                var wordsFound = searchForWord(htmlBody, SEARCH_WORD); //Search for words found in SEARCH_WORD
                if(wordsFound.length > 0) {
                  var captured = captureDomNodes(url, wordsFound, $, null, SEARCH_WORD); //Capture each Dom Nodes
                  resolve(captured);
                } else {
                  resolve([]);
                }
              });
            })
          }))
          .then((result) => {
            return Watson.toneAnalysis(result);
          })
          .then((testresult) => {    
            return testresult;
          })
          .catch((error) => {
            return error;
          });
        }
      {% endhighlight %}
      </div>
    </div>
	</section>
</section>
