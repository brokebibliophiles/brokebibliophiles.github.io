---
title: UI Current State and Thoughts - 1
subtitle: demo.scribbledata.io as it currently stands
comments: true
---

<p>The following are the various screens we have so far for our reference. I don't have a private repo to host this on but this is relatively inconspicious, no proprietary information and won't be found as a page so I'm fine hosting it here for now. </p>


### Before Logging In 
- Color shades in use  : 
	- <b>Background colors</b> : [#2c3e50](https://www.google.com/search?client=ubuntu&channel=fs&q=%232c3e50&ie=utf-8&oe=utf-8) for the header, white for the body
	- <b>Text Colors</b> : white for the header , [#18bc9c](https://www.google.com/search?client=ubuntu&hs=JV0&channel=fs&ei=LCUYW-KrNIvPvgSN_KjQBA&q=%2318bc9c&oq=%2318bc9c&gs_l=psy-ab.3..0j0i30k1l2.73197.73197.0.73938.1.1.0.0.0.0.83.83.1.1.0....0...1c..64.psy-ab..0.1.82....0.V0ZcwB75A2E) on hover, #2c3e50 for the body
- Buttons : 
	- <b>Sign Up</b> : Title: Sign Up. Details requested - Username(mandatory), First Name, Last Name, Email Address(Mandatory), Password, Captcha
	- <b>Log In</b> : Title: Sign In (?). Username, password. Standard stuff.
	- <b>Continue</b> : Takes you to the Log In page and redirects to the Signed in page.
- 3 columns : 
	- <b>Ingest Data</b> :  Should we say "Any Volume" or provide realistic SLAs?
	- <b>Run Models</b> : Sounds fine. (Preset instead of BuiltIn?)
	- <b>Deliver</b> : - 

<p align="center">
<img src="../../img/scribble/1.png"></p>

### After Logging In :

- Can do away with the 3 columns. They already know our offerings at this point. But what else to put in its place? 
- Options on Nav Bar :
	- Execution : 5 sub-items
		- Execution Status (Is this paginated? How much history do we allow? Should this be informed? )
		- Adhoc Commands
		- Application Log (Same questions as in Execution Status)
		- Activity Log (Can we call it User Activity Log?)
		- Data Exports (Data export activity? We don't allow exporting data in this view)

	- Status: 4 sub-items
		- Health
		- License
		- Data Sources
		- Resource Monitor

	- Developer : 2 sub-items
		- API
		- SDK(Experimental)

	- Resources : 6 sub-items (Length of list is slowly increasing :D )
		- Operations
		- Security
		- News
		- FAQ
		- About
		- Help

	- Logged In User's name : 3 sub-items
		- Profile
		- Invite Colleagues
		- Logout

	- Admin (To be ideally displayed only if the user is the admin)

<p align="center">
<img src="../../img/scribble/2.png"></p>

## Design notes

From the sites I've gone through and talking to my friends, this is what I've picked up so far. And these seem intuitive but they're easily missed.
Ideally, a website, even a B2B page should tell a story. 

- If I press the Continue button, I get the organizational view. Can we replace this with that information directly if this screen is superfluous post-login? 
- What is my priority/order of checking in terms of the various tabs on the Nav-Bar when I log in?
E.g. - Considering something as rudimentary as Sublime Text or its inferior cousin, Notepad - File comes first and then comes Edit. These are things I will use all the time and eventually resort to hotkeys. (Are hotkeys too far-fetched in our application?)
- Anything that is static information that is unlikely to change over iterations should be shunted to the end - for e.g. - License, About, Help.
- Many friendly websites also have a pop-over the first time they're used, displaying the various options that can be used. For e.g - GMail, Evernote, Dropbox. Granted, these are B2C, but even the users who use a B2B product such as ours will probably appreciate it. 
Asana, for example is both B2B and B2C, and it has animated tips that flit over in turn.
<p align="center">
<img src="../../img/scribble/6.png"></p>
<p align="center">
<img src="../../img/scribble/7.png"></p>
- What if there are features that are offered over and above their current paying slab? They should be aware of it so they can avail it at some point. Even if this is intended as a utilitarian site and not the main business facing website, this can be a part of the "Profile" info so they can view those features and they can request the admin if that's a necessity (This might be overkill.)
- Based on the role of the user, the FAQ should link to the Operations page or the current FAQ page. As an engineer, I'm more concerned about the technical operations than the offerings of the parent company. 

As far as color schemes go - there are color wheels and the governing principles of color models - Monochromatic i.e. Shades, Triad, Complementary etc. There are a lot of helpful sites that we can refer to help us get the shades that are said to complement each other - 
- [http://www.paletton.com/](http://www.paletton.com/)
- [https://color.adobe.com](https://color.adobe.com)

We need to zero in on what colors we, ScribbleData, as a company hold dear. The Blue and White of the existing logos are beautiful but we definitely can have two sets of colors for two different platforms. 

Venkata suggested that I take a look at Sentry the other day and considering that as a rudimentary case and using the color palettes from the aforementioned sites, this is how the new UI currently looks. Obviously, the design suggestions I've spoken about are yet to be discussed further and implemented. 
But here it is as it stands - 


<p align="center">
<img src="../../img/scribble/3.png"></p>

<p align="center">
<img src="../../img/scribble/4.png"></p>

<p align="center">
<img src="../../img/scribble/5.png"></p>

I personally liked AdminLTE a lot. It seems...sleeker. But yes, the color scheme and layouts will depend on the content. The content depends on the utility. 


All of this is very much a work in progress. I'm still learning more WRT usability, layouts, screens and docks as to how B2B percieve it. I will add to this. 

PS - I'll put this in a mail over the weekend for our reference. I hope this format is okay for now.

{% if page.comments %}
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = abhiramr.github.io/scribble/01_UI_Observations_1;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = scribble/01_UI_Observations_1; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://abhiramr.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}
