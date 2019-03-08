These bookmarklets are for use with reddit. They're particularly useful to moderators.


Submit currenty displayed userpage to /r/botbust:

```javascript
javascript:(function(){var user=document.URL.match(/\/(user|u)\/(([a-zA-Z_0-9\-]*?)+\b)/);window.location.href="http://www.reddit.com/r/botbust/submit?resubmit=true&title=overview for "+user[2]+"&url=http://reddit.com/u/"+user[2]})()
```


Mail current, on-screen page to Reddit Admins:

```javascript
javascript:(function(){var currentUrl=document.URL;window.location.href="http://www.reddit.com/message/compose/?to=/r/reddit.com&subject=spammer&message="+currentUrl})()
```


Submit current, on-screen page to reddit:

```javascript
javascript:(function(){var currentUrl=document.URL;window.location.href="http://www.reddit.com/submit/?resubmit=true&url="+currentUrl})()
```


Open banned page of current subreddit:

```javascript
javascript:(function(){var url=document.URL.match(/\/r\/[a-z0-9_]+/i));window.location.href="http://www.reddit.com"+url+"/about/banned"})()
```


Send Modmail with link to current reddit page to the modmail of the subreddit you're viewing:

```javascript
javascript:(function(){var sub=document.URL.match(/\/r\/[a-z0-9_]+/i);window.location.href ="https://www.reddit.com/message/compose?to=/r/"+sub+"&subject=So&message="+document.URL})()
```


Translate current browser's URL to a QR:

```javascript
javascript:location.href='http://chart.apis.google.com/chart?cht=qr&chs=300x250&chl='+encodeURIComponent(location.href)
```
