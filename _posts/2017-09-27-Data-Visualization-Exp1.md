### Hours of max FB Usage —
I originally intended to do something else, but ended up doing this instead  —  Figuring out at what hours during the day I’ve been most active on Facebook — outliers included.

##### How?

- Downloaded my entire Facebook data - This can be done using the Facebook APIs or using the less painful way — requesting for a copy of your Facebook data as a zip file from your Settings panel.

- Scraped this local webpage’s timeline section after hosting it on a local server with a simple Python script using Scrapy and extracted only the timestamps for all the posts and stored it in a CSV.

- Parsed this data (a modest dataset of 8500+ entries) and fetched the timestamps taking heed of AM and PM and storing this data in another CSV.

- Segregated this data into hourly ranges e.g. 1am-2am, 2am-3am , for all 24 hours and obtain the cumulative count of entries per hour and store this in another final CSV. Surprisingly, MS-Excel was very helpful in this venture.

- The CSV from Step 4 served as input to the D3.JS bubble chart script (Courtesy Mike Bostock’s bubble chart template, with some tweaks).

The result was this gloriously satisfying and insightful bubble chart.

![GitHub Logo](https://raw.githubusercontent.com/abhiramr/Old_Website_2/master/images/01_data_viz_1.png)

***


### What does this show?
The colors have no bearing, but the sizes of the bubbles indicate the number of posts, well, posted in that hour — the larger bubbles indicating more activity during that period and the smallest ones being the least amount of activity in that hour. The inference being that I have wasted a tremendous amount of time on Facebook during almost every hour of the day over the last 9 year time-period for which this data was obtained, save for the 2am — 6am mark. This also illustrates a seemingly poor sleep pattern.

### What haven’t I taken into account?
A lot of people post on my wall on Facebook on my birthday. But this number which varies around the 100–150 mark every year is scattered across all hours (around 10 posts approx. every hour) of the day and this outlier, I feel, can be safely neglected.

### What’s next?
I’m hoping to glean some more insights (useful ones hopefully) from this data and will post the results as a follow-up to this blog.


Feel free to try this out for yourself if you’re interested in insights that you can probably intuitively already find out without going through this procedure or are just looking to wade into the basics of Data Visualization just to feel like you’ve started something rudimentary along these lines for your satisfaction ..like I did.

##### Reference material —
https://www.facebook.com/help/302796099745838 https://doc.scrapy.org/en/latest/topics/shell.html
https://bl.ocks.org/mbostock/4063269

##### Source Code —
https://github.com/abhiramr/DataViz/tree/master/Fb_Usage
##### Also Published In —
[Hacker Noon](https://hackernoon.com/data-visualization-experiment-1-f34a10679b8)

{% if page.comments %}
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = abhiramr.github.io/2017-09-27-Data-Visualization-Exp1;  // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = 2017-09-27-Data-Visualization-Exp1; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
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
