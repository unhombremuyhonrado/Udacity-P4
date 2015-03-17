## Website Performance Optimization portfolio project

Here is my submission for Udacity’s Front-End Web Developer Nanodegree. Project 4: Website Optimization.
 
Our objective was to take Cameron’s portfolio [http://unhombremuyhonrado.github.io/Udacity-P4/ ] and optimize it to score above a 90/100 on mobile devices and desktop browsers via Google’s PageSpeed Insights [https://developers.google.com/speed/pagespeed/insights/]
 
This project was particularly challenging, but with the following tweaks I was able to  score a 97/100 on desktop browsers and mobile results to 95/100. I also did A LOT of extra stuff that was COMPLETELY unnecessary. I think I did this, in part, because I was very confused about this until I took the course again. I didn’t feel like starting ALL over (again) so I just went nuts with it.
 
The following steps (most likely NOT in this order) were taken:

In-lined all CSS and minified BOTH index.html and pizza.html.

Added media print and minified that sucker.

Added async to all JavaScript links on index.html and (why not) pizza.html. Also, this wasn’t requested.

Compressed all images on this page and on pizza.html. I used

In-lined all CSS on pizza.html (not sure why, as it doesn’t even affect fps).

Minified the hell out of most css, js and html files in index.html and pizza.html

Removed a massive-amount of unused css stuff from bootsrap, then I minified it, again.

Refactored updatePositions function, then added requestAnimation to it

Improved fps of scroll performance by removing .mover query from function.

Used translateX trick found in piazza posts.

References: 
https://developer.chrome.com/devtools/docs/timeline
https://plus.google.com/events/comnga3cdvrpkjm7dvb4l71ph2o?authkey=CPbhlNSdtpiEDg
http://addyosmani.com/blog/making-a-site-jank-free/
http://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/ [this one obviously really helped]
http://css-tricks.com/tale-of-animation-performance/
http://joshondesign.com/p/books/canvasdeepdive/chapter05.html [KIND OF HELPED]
http://csstriggers.com/ [This site provides a breakdown of how each css property affects layout, paint and composite.]
http://benfrain.com/improving-css-performance-fixed-position-elements/
http://jankfree.org/
http://davidwalsh.name/translate3d [force hardware acceleration]
http://www.html5rocks.com/en/tutorials/speed/layers/
http://aerotwist.com/blog/on-translate3d-and-layer-creation-hacks/
https://developer.chrome.com/devtools/docs/rendering-settings
http://creativejs.com/resources/requestanimationframe/
http://css-tricks.com/css-media-queries/
https://developers.google.com/web/fundamentals/layouts/rwd-fundamentals/use-media-queries
https://imageoptim.com/
http://www.html5rocks.com/en/tutorials/speed/rendering/#toc-raf [APPLYING RAF]
http://creativejs.com/resources/requestanimationframe [APPLYING RAF]
http://www.html5rocks.com/en/tutorials/speed/animations/ [APPLYING RAF]
http://www.webreference.com/programming/javascript/jkm3/index.html

References for 60fps optimization
https://developer.chrome.com/devtools/docs/rendering-settings
https://docs.google.com/presentation/d/1CH8ifryioHDLT1Oryyy8amusUmq2FytpCPCpk0G3E4o/edit?pli=1#slide=id.p

http://www.allreadable.com/3d5a6iIO 
https://www.youtube.com/watch?v=YyQYhhy1dZI
http://blog.teamtreehouse.com/increase-your-sites-performance-with-hardware-accelerated-css
http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/

PIAZZA POSTS FROM:
11/17/2014
01/15/2014
01/09/2014
Finding better framerate: https://piazza.com/class/i0sf6tsmg0r7do?cid=1017



Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

### Sample Portfolios

Feeling uninspired by the portfolio? Here's a list of cool portfolios I found after a few minutes of Googling.

* <a href="http://www.reddit.com/r/webdev/comments/280qkr/would_anybody_like_to_post_their_portfolio_site/">A great discussion about portfolios on reddit</a>
* <a href="http://ianlunn.co.uk/">http://ianlunn.co.uk/</a>
* <a href="http://www.adhamdannaway.com/portfolio">http://www.adhamdannaway.com/portfolio</a>
* <a href="http://www.timboelaars.nl/">http://www.timboelaars.nl/</a>
* <a href="http://futoryan.prosite.com/">http://futoryan.prosite.com/</a>
* <a href="http://playonpixels.prosite.com/21591/projects">http://playonpixels.prosite.com/21591/projects</a>
* <a href="http://colintrenter.prosite.com/">http://colintrenter.prosite.com/</a>
* <a href="http://calebmorris.prosite.com/">http://calebmorris.prosite.com/</a>
* <a href="http://www.cullywright.com/">http://www.cullywright.com/</a>
* <a href="http://yourjustlucky.com/">http://yourjustlucky.com/</a>
* <a href="http://nicoledominguez.com/portfolio/">http://nicoledominguez.com/portfolio/</a>
* <a href="http://www.roxannecook.com/">http://www.roxannecook.com/</a>
* <a href="http://www.84colors.com/portfolio.html">http://www.84colors.com/portfolio.html</a>
