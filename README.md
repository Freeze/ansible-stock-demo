# ansible-stock-demo

This was made for a demo of some of the things you can do with Ansible for a demonstration at work.

### This playbook will do the following: ###
- Grab a list of stock tickers to check from [my GitHub repo](https://raw.githubusercontent.com/Freeze/ticker-list/master/list.json)
- Create an ansible-friendly fact called `result_friendly`
- Loop through all of the symbols listed in `result_friendly` and perform lookup on each using [Alphavantage's free API](https://www.alphavantage.co/documentation/)
- Create a new Quote:Price dictionary with the data gathered from the above queries
- (Here is where it gets just stupid) Delete an `index.html` if it is found in your playbooks directory
- Create a new `index.html` based on `templates/index.html.j2` which loops through our Quote:Price dict and adds them all to a webpage
- Upload the webpage to my website, holden.gg.  (The computer I am running this from has a key for that server on it, this will not work for you)

> Holden, you included a vault file on a public repository!  

Sure, I did.  But you know what, all that is in it is a free API key and a message congratulating you if you break it.  I'm really not to worried.  The keys to my kingdom are not in it.
