dpd-pushnotifications
=======

A very simple Deployd Resource for connectivity to the Google Cloud Messaging (GCM) and Apple Push Notification Service (APNs)

Include in your package.json like
<pre>
  "dependencies": {
    "dpd-pushnotifications": "git+ssh://git@github.com:ozzroach/dpd-pushnotifications.git"
  }
</pre>
then do
<pre>
npm install
</pre>
Usage in a Deployd-Event-Handler:

For Android:
<pre>
dpd.pushnotifications.post({
		gcmRegistrationIds: ["...", "..."],
		title: "...",
		message: "...",
		msgcnt: "...",
		soundname: "...",
		collapseKey: "...",
		delayWhileIdle: true,
		timeToLive: 4000
	},
	function (err, results) {
    	console.log(results);
	}
)
</pre>
For iOS:
<pre>
dpd.pushnotifications.post({
		apnTokens: ["...", "..."],
		message: "...",
		msgcnt: "...",
		soundname: "...",
		timeToLive: 4000
	},
	function (err, results) {
    	console.log(results);
	}
)
</pre>