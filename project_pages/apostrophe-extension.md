## Apostrophe Browser Extension

<p>Apostrophe is a browser extension that I have developed for use with Google Chrome and the open-source Chromium that it is based on.  Apostrophe allows the user to search all of the links on a given page to see if it matches some given text, as well as to navigate in this means.</p>

<p>In simpler terms, it is a quick and dirty means to replicate the "Quick Find" keyboard shortcut for Firefox that allows for very keyboard-heavy navigation and use.</p>

<p>GitHub: <a href="https://github.com/spopkin/apostrophe">https://github.com/spopkin/apostrophe</a></p>
<p>Chrome Web Store: <a href="https://chrome.google.com/webstore/detail/apostrophe-navigation-ext/flddhoonfbaphfihmkoklkghmhmdhemh">https://chrome.google.com/webstore/detail/apostrophe-navigation-ext/flddhoonfbaphfihmkoklkghmhmdhemh</a></p>

## Why Do It?

<p>My main Linux laptop has a slow, but dual-core CPU.  As such, it is decent at multiprocessing and multithreaded functionality, but not so good at heavy number crunching on a single thread.</p>

<p>While both Chrome and Firefox both support multiprocess functionality, the privacy extensions that I like to install disable it on Firefox, making Chrome/Chromium perform better on my laptop.</p>

<p>As such, I aim to switch to Chromium (Chrome's open source base) for a little while, at least until Firefox catches back up.  Unfortunately, navigation purely by keyboard is a little bit of a pain in Chromium and Chrome, as they lack Firefox's link search shortcut.</p>

<p>Since I am someone who likes to optimize his workflow anyway, I took this opportunity to make an extension to do what I want.</p>

## How it is Used

<p>The extension adds an invisible search bar to every page, which is made visible by pressing the apostrophe key.</p>
<p>Pressing the escape key will close the search bar.</p>
<p>While the search bar is focused, any text typed by the user will be searched for in all of the links in the page.  The first instance will be highlighted.</p>

<p>Pressing Enter will click on the selected link.  Ctrl-Enter opens the selected link in a new tab.</p>

<p>F2 can be used to cycle through all of the links that match the typed text.</p>

## List of Technologies and Techniques Used:
<ul class="TechList">
	<li>HTML 5</li>	
	<li>CSS 3</li>	
	<li>JavaScript</li>	
</ul>

## How it Works
<p>Basically, the extension is based around a Chrome extension content script.  This script loads on every website served over http or https.</p>

<p>It keeps track of variables such as the most recently searched for text and most recently selected link and registers a keyboard event listener connected to a handful of functions that alter the variables accordingly.  It's a bit of a messy system, but it more or less follows an "observer" model.</p>

## Design Decisions
<ul class="TechList">
	<li>It uses the event listener to be able to observe key presses.</li>
	<li>I used JavaScript, since Browser extensions tend to support that well.</li>
	<li>I used the "observer" development model, as this script needed to react to key presses.</li>
</ul>

<a href="projects.html">Return to projects page.</a>

<br/>
<br/>
<br/>
<br/>
<br/>
