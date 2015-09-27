These bookmarklets are for use with reddit. They're particularly useful to moderators.


Submit current userpage to /r/spam:

```javascript:(function(){var user = document.URL.match(/\/(user|u)\/(([a-zA-Z_0-9\-]*?)+\b)/);window.location.href = "http://www.reddit.com/r/spam/submit?resubmit=true&title=overview for "+user[2]+"&url=http://reddit.com/u/"+user[2]})()


Open banned page of current subreddit:

	javascript:(function(){var url = document.URL.match(new RegExp("/r/[a-zA-Z0-9_\-]*"));window.location.href = "http://www.reddit.com" + url +"/about/banned"})()


Send current page to Admin:

	javascript:(function(){var currentUrl = document.URL;window.location.href = "http://www.reddit.com/message/compose/?to=/r/reddit.com&subject=spammer&message="+currentUrl})()


Modmail current page to the subreddit you're on, using scraping:

	javascript:(function(){var sub = document.URL.match(/\/r\/[a-z0-9_]+/i);window.location.href ="https://www.reddit.com/message/compose?to=/r/"+sub+"&subject=So&message="+document.URL})()


Modmail current page to the subreddit you're on, using JQ:
	
	jjavascript:(function(){var sub = $('.redditname a').first().text(); var url = document.URL;window.location.href = "http://www.reddit.com/message/compose/?to=/r/"+sub+"&subject=so"+"&message="+url;})()


Submit current page to reddit:

	javascript:(function(){var currentUrl = document.URL;window.location.href = "http://www.reddit.com/submit/?resubmit=true&url="+currentUrl})()
	

Translate current URL to a QR:

	javascript:location.href='http://chart.apis.google.com/chart?cht=qr&chs=300x250&chl='+encodeURIComponent(location.href)


