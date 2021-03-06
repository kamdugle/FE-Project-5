
# Project 5 Readme

## Summary

This is a website developed by Udacity as part of its Frontend Developer training. Two pages on the website were optimized in order to demonstrate optimization of page load times and smooth animations.

## Instructions

To view the project, download the zip file, extract, and open the index.html within the distro subfolder on your local server. To view the original, non-optimized version of the site, open the index.html in the src subfolder instead.

To view the page optimized for a quick page load, view the landing page landing page. This page was optimized to achieve a 90 PageSpeed score from PageSpeed Insights. Optimizations made are discussed below.

To view the page optimized for smooth animation, click on Cam's Pizzeria. Two animations are vieweable. The first is parallax scrolling pizzas in the background, which can be viewed by scrolling. The second is resizing of pizzas in the "Our Pizzas" section. This can be seen my dragging the size scroller underneath the "Our Pizzas" heading.

## Optimizations made

### Pageload
Inlined javascript to load the web font used on the page rather than waiting for an outside link.

Inlined css to avoid waiting for that to load.

One image was way too large, and was being resized by brute force, so I re-sized the actual jpg to avoid having to download extra image data for no benefit.

Generally optimized images.

### Animation

Re-wrote loops to forcing synchronous layout that was occuring both in background pizza animation and in re-sizing of pizzas in our-menu.
Set the parallax animation to fire from requestanimationframe, which in turn fires from scroll event. Previously the two were linked directly. Replace querySelectorAll with getElementsByClassName in various sections. Moved pizzasDiv definition out of loop. Moved phase definition in parralax routine out of the write loop. Made number of parallax pizzas generated depend on viewport size, and moved a constant variable calculation out of loop. Also added some css to style.css to forced GPU to become active.

## Gruntfile

As part of the project, grunt was made use of. The gruntfile was loaded as part of the repository. However, the gruntfile was used in a fairly manual manner, not with a proper automated workflow, so there is not a straightforward way to run it to arrive at the distribution version of the website from the source file. However, below are notes on the components made use of in the gruntfile: 

### imagemin

https://github.com/gruntjs/grunt-contrib-imagemin

imagemin was used to optimize images on the main landing page.

### htmlmin

https://github.com/gruntjs/grunt-contrib-htmlmin

Htmlmin was used to minimize the html, sacrificing readability.

### responsive-images

https://github.com/andismith/grunt-responsive-images

In general, this script can be used to create responsive images for different versions of the site, but I used it to resize images that were overly large.