---
is_a_project: true
description: A multi-PDF search utility
---
## PDF RuleFinder
<p>The PDF RuleFinder is a simple Node.js-based utility that is used to find the page in a set of pdf files that best matches a set of keywords.  Essentially, it's used for searching D&D PDFs to try to find specific rules based on passed keywords</p>

<p>This project is actually the first of a broader set of tabletop gaming utilities that I intend to work on.</p>

<p>GitHub: <a href="https://github.com/spopkin/Dungeon-Master-Toolkit">https://github.com/spopkin/Dungeon-Master-Toolkit</a></p>

## List of Technologies and Techniques Used:
<ul class="TechList">
	<li>HTML 5</li>	
	<li>CSS 3</li>	
	<li>Node.js</li>	
	<li>JavaScript</li>	
	<li>JQuery</li>	
	<li>MongoDB</li>	
	<li>REST</li>	
	<li>Express</li>	
	<li>pdf-text-extract library</li>	
	<li>Wait.for fibers library</li>	
</ul>

## How it Works
<p>When started with the --refresh-db flag, it uses pdf-text-extract to extract the text from all of the PDF files in a preconfigured rulebook directory.  After the text is extracted, it is inserted into entries for each given book in MongoDB.  Later, when the function to search is invoked, it searches through those extracted text entries and ranks them in terms of which page is the most likely to correspond to the searched-for keywords.</p>

<p>The frontend is an HTML, CSS, and JavaScript page that uses JQuery to retrieve information from the NodeJS REST API.</p>

## Design Decisions
<ul class="TechList">
	<li>It is a Node.js webapp to simplify future integration with other tools that I plan to make</li>  
	<li>It uses MongoDB, as the data used is just a bunch of documents</li>
	<li>It preloads the text data for performance reasons</li>
</ul>

<br/>
<br/>
<br/>
<br/>
<br/>
