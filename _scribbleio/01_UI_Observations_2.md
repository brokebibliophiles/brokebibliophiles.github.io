---
title: UI Current State and Thoughts - 2
subtitle: More usecases, styles, colors etc.
comments: true
---

So basically in perusing all the UX and UI sites that I did, the bottomline is again, to understand what problem we're solving - What is the goal?
- To inform? ("Learn from me")
- To grab attention? ("Look at me")
- To enable? ("Use me").

Our site falls in the third category for the most part, but we also have some sections in the site that category (2) and (3) fit in i.e. Resources like Whitepapers or FAQs fall in the "information" category and error alerts or Command History, Execution status etc fall in the "needing attention" category.


### First Time Users -


As far as the internal UI and UX of B2B websites go, the accessibility from a outsider's POV is quite low unless you become a customer. However here are a few more examples of elements we can use like the initial tips from Asana.

- Instead of one-time tips,  [Figma](https://www.figma.com/) has an on-loop GIF that shows the features you can use in the product.

<p align="center">
<img src="../../img/scribble/scribble_01.gif"></p>

- [Invision](https://www.invisionapp.com/) does two things well :
	- It doesn't assume that you don't know stuff but asks you to watch a video if you want help with how to start or reach out to the Help Center that links me to 3 screens - "Getting started", "Knowledge Base" and "Community". The first two options are a given, but the last option can be useful to us in future when multiple people within a company use our product and want to clarify internal repetitive doubts. Since every customer of ours might have their own usecases of usage of our product, they might need a space where they can dump all their findings there for easy reference before reaching out to us - An internal, implicit support team if you will. 
	- It shows their platform's status on the [Support](https://support.invisionapp.com/hc/en-us) page - as a green dot on the header to indicate if all systems are operational, for example. I'd assume the dot goes orange or red based on any failing cases.

<p align="center">
<img src="../../img/scribble/26.png"></p>

<p align="center">
<img src="../../img/scribble/25.png"></p>



- There are other sites as well that are a little more..playful. They have curved arrows/tool-tips that point to the different paths that can be taken etc. Given the creative nature of our base website, I think we can afford to do this as well. These arrows trace a path similar to the way Asana does things, but it will be less rigid in its appearance. 

More info here - [https://www.appcues.com/blog/user-onboarding-ui-ux-patterns](https://www.appcues.com/blog/user-onboarding-ui-ux-patterns)


### Minimum Navigation, Maximum Visibility & Reusability - 

The user of the page should be able to find what he needs with the least number of clicks.
Also, from a developer perspective, we should be able to use this code for all future customers as well with minimal work.

<p align="center">
<img src="../../img/scribble/23.png"></p>


The parameters every website with a good UX element set is measured by are : 
- size
- color
- layout
- spacing
- flow

This elemental set is what a pattern library in every company should define so that any future designs will always use this library as reference.

#### Size : 
Headers, content and footers should have set sizes. These values differ across implementations but Bootstrap 4 has a pretty solid lineup with values that seem to be agreed upon in most websites that use it. 

- [Bootstrap Typography](https://getbootstrap.com/docs/4.1/content/typography/)
- [https://www.w3schools.com/bootstrap4/bootstrap_typography.asp](https://www.w3schools.com/bootstrap4/bootstrap_typography.asp)

<b>Fonts</b> preferred by B2B websites are generally under the Sans Serif umberella. [This was an interesting exchange on the topic](https://www.marsdenmarketing.com/blog/bid/182246/The-Impact-of-Fonts-on-B2B-Website-Design-and-Branding)

#### Color : 

Like I mentioned in the earlier article, a company's thematic colors are key. For example,

- Future Group! - Orange and White
- LinkedIn - Blue and White 
- Dropbox - Blue and White
- Google - White and the primary colors for text.

If, for each customer, the idea is to retain Scribble's underlying identity, then we will also need to maintain consistent color themes across each offering. The Logo is another mark of consistency to be followed. We currently have the entire text "scribbleData" on the logo on our [main page](https://www.scribbledata.io/). This should be reflected in the Admin page as well, in addition to the minified icon version, perhaps in the extended form of the sidebar.

If however, we intend for the customer to embed his assets as a part of the service we offer him (as is the case sometimes), then we will have to fall back to their ..colors, so to speak. 

Most websites have a hint of blue in them. And [this article](https://uxplanet.org/the-most-important-color-in-ui-design-d4f23aefffdf) makes a good case for why that is. There is also the [60-30-10 rule](https://blog.prototypr.io/how-to-use-colors-in-ui-design-16406ec06753) to be accounted for where 60% is the dominant hue, 30% is the secondary color and 10% is for the accent color. This rule originated in interior designing initially but it apparently makes sense for the web as well and is followed widely. 

- Other links : 
	- [https://coolors.co/](https://coolors.co/)

#### Layout : 

Most websites boasting good UI and UX implicitly follow the Gestalt principles categorized by Proximity, Similarity, Continuity, Closure and Connectedness. The buzzwords aside, what it means is that things that belong together stay together. 
Proximity and Continuity are the most that apply to our website since say, everything related to Execution should belong together (as it currently does) but there also needs to be a continuity among elements i.e. if the task of Daily Backup is intended to be followed by a API Sync Task, they need to be placed in that order for easy continuity.

There are also instances where each group of features are assigned a different color, each highlighted and important in its own way and yet each markedly separate. 

<p align="center">
<img src="../../img/scribble/22.png"></p>

### Libraries -

- Bootstrap 4 claims to be faster than Bootstrap 3 having migrated to Sass format from LESS. 
It also offers easier navigation and dropdown support, but a slightly more cumbersome pagination. I think I can go ahead and try it out in a couple of views. 
- Material Design is available for Bootstrap 4 as well and there are free libraries for the same. I haven't implemented any sample pages in this either. I'll comment on the ease of adaptability once I've tried it out over the weekend.
	- [https://mdbootstrap.com/](https://mdbootstrap.com/)
	- [https://fezvrasta.github.io/bootstrap-material-design/](https://fezvrasta.github.io/bootstrap-material-design/)

For now, I'm leaning more towards using Bootstrap 4. There's no doubt that it offers more than Bootstrap 3 even if Just the speed of compilation is to be considered.

### Misc Thoughts and Links -

- For the FAQ / Whitepapers / Docs section, some sites have a "Was this helpful?" box so users can let us know if they needed more information over and above what was provided.
<p align="center">
<img src="../../img/scribble/24.png"></p>
- It will be nice to collect anonymised data on the options used by users on a regular basis, so we know where the heat is focussed the most.
- Will we need to add a "Cookie agreement" box upfront when the page loads for the first time?
<p align="center">
<img src="../../img/scribble/16.png"></p>
- This is a really good link for everything on Typography - [http://thinkingwithtype.com/](http://thinkingwithtype.com/)

{% if page.comments %}
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = abhiramr.github.io/scribble/01_UI_Observations_2;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = scribble/01_UI_Observations_2; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
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