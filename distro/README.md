
# Project 5 Readme

## Summary

This is a website developed by Udacity as part of its Frontend Developer training. Two pages on the website were optimized in order to demonstrate optimization of page load times and smooth animations.

## Instructions

To view the project, download the zip file, extract, and open the index.html within the distro subfolder on your local server. To view the original, non-optimized version of the site, open the index.html in the src subfolder instead.

To view the page optimized for a quick page load, view the landing page landing page. This page was optimized to achieve a 90 PageSpeed score from PageSpeed Insights. Optimizations made are discussed below.

To view the page optimized for smooth animation, click on Cam's Pizzeria. Two animations are vieweable. The first is parallax scrolling pizzas in the background, which can be viewed by scrolling. The second is resizing of pizzas in the "Our Pizzas" section. This can be seen my dragging the size scroller underneath the "Our Pizzas" heading.

## Optimizations made

### Pageload

### Animation

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