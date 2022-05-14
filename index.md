<h1 align="center">Astral API</h1>
<div class="section-block">
	<div class="answer">
		<div class="text-block"> Before you get started using Astral, there is some basic knowledge you will need to know about. Astral does not require an API Key, which allows for free public access across our entire platform. We adjust our rate limits frequently to match our users needs. </div> Astral is still very early in development, so the things we offer may change. So far we offer:
<div class="section-block">
	<div class="answer">
		<div class="text-block">
			<h2 class="endpoint-title">Database Search</h2> <pre><code class="language-plaintext">https://beta.database.report/api/search/{target}/{type}</code></pre>
			<p>Send a query request and output all breaches into a format of <code>type</code></p>
			<h4>target:</h4>
			<ul class="no-list">
				<li>target can be an email address, username, password or really anything you'd like</li>
			</ul>
			<h4>type:</h4>
			<ul class="no-list">
				<li>json - output into a prettify'd JSON list</li>
				<li>plain - get a plaintext output</li>
				<li>none - defaults to <code>json</code> outputs</li>
				<ul> </ul>
			</ul>
		</div>
		<pre><code class="language-plaintext">GET https://beta.database.report/api/search/magicmanlogan@gmail.com/json</code></pre> <b style="color: rgb(200,200,200);">Response:</b> <pre><code class="language-json" style="width: 100%;">{
  "response": "success",
  "results": [
    {
      "minecraft_hacked_logins": "magicmanlogan@gmail.com:loganrocks - Rogen"
    },
    {
      "ogusers.com_dehashed": "magicmanlogan@gmail.com:loganrocks"
    }
  ]
}</code></pre> </div>
</div>
<div class="section-block" id="minecraft">
	<div class="section-block">
		<div class="answer">
			<div class="text-block">
				<h2 class="endpoint-title">Minecraft Search</h2> <pre><code class="language-plaintext">https://beta.database.report/api/search/{target}/{type}</code></pre>
				<p>Send a query request and output all minecraft logs into a format of <code>type</code></p>
				<h4>target:</h4>
				<ul class="no-list">
					<li>target can be an email address, username, or UUID</li>
				</ul>
				<h4>type:</h4>
				<ul class="no-list">
					<li>json - output into a prettify'd JSON list</li>
					<li>plain - get a plaintext output</li>
					<li>none - defaults to <code>json</code> outputs</li>
					<ul> </ul>
				</ul>
			</div>
			<pre><code class="language-plaintext">GET https://beta.database.report/api/minecraft/{target}/{type}</code></pre> <b style="color: rgb(200,200,200);">Response:</b> <pre><code class="language-json" style="width: 100%;">{
  "response": "success",
  "results": [
    [
      "DatPixel_Emails_DB.csv.txt",
      "batuhan-un@hotmail.com,Notch,360"
    ]
  ]
}</code></pre> </div>
	</div>
	<div class="section-block" id="news">
		<div class="answer">
			<div class="text-block">
				<h2 class="endpoint-title">News / Updates</h2> <pre><code class="language-plaintext">https://beta.database.report/api/news</code></pre>
				<p>Get a JSON formated list of updates we've made to our APIs' and website</p>
				<b>Response:</b> <pre><code class="language-json" style="width: 100%;">{
  "05/03/22": "The site is now online, we are improving speeds and website protections rapidly!",
  "05/04/22": "Added user plans and made API semi-public."
}</code></pre> </div>
		</div>
	</div>
</div>
</section>
