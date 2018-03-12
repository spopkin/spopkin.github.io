## Betaversity Buildathon
<p></p>

## This Project is Pretty Tiny
<p>It is actually small enough that I would not have included it here, if not for the fact that it has a good story attached to it.</p>

## The Story Behind This Project
<p class="Summary"><strong class="InlineBoldWords">Summary:</strong> I managed to reach the semifinals by building something using unfamiliar tools in the last few hours of a two-week buildathon, despite having zero supplies and experience.</p>

<p>As I was returning from class one day, I encountered a shipping container with windows in the middle of campus.  As I walked past, I noticed 3D-printers in the windows and that the doors to the container were open.  There were people inside, working with electronics hardware.</p>

<p>As all of this had piqued my curiosity, I asked about it and discovered that they were there running a buildathon that had been going on for two weeks.  All participants are given a free microcontroller to build whatever they want.  Contestants who logged something cool enough on the website that was being beta-tested, would advance to the semifinals. The deadline to do so was midnight that night.  As someone who is interested in embedded software development, who had already learned how to code in C, I opted to join in on the contest.</p>

  <p>Later that night, after the tool installations had finished and I had completed that day's homework, it was time to start work on the Buildathon.  It was 8:00PM and I needed to think of a project to create, actually create it, and document it well enough to compete with projects that had as much as two weeks worth of work poured into them.  I opted to do a simple egg timer, as I had no electronics components whatsoever that I could use with the board.</p>

<p>Perhaps I was only one of a few people who managed to figure out how to use the tools in time to get any actual work done, as I received an email the next day stating that I was a semifinalist.  While I ultimately did not win the contest, I did get a free microcontroller board, a good story, and a chance to play with embedded software development.</p>


## It's Not on GitHub
<p>Unfortunately, this project required that I check my code into a betaversity website.  As I was not yet in the habit of using my GitHub profile, it is not on here.  If I find the code somewhere in a forgotten corner of my filesystem, I do plan to put it on my GitHub account.</p>
<p>While it is not on GitHub, I did create a Youtube video demo of the end result, which is embedded below.</p>

<div style="position:relative;height:0;padding-bottom:56.25%"><iframe src="https://www.youtube.com/embed/Qv3vtAFT1VI?ecver=2" style="position:absolute;width:100%;height:100%;left:0" width="640" height="360" frameborder="0" allowfullscreen></iframe></div>


## List of Technologies Used:
<ul class="TechList">
	<li>Texas Instruments MSP430 FR5969 Microcontroller Board</li>	
	<li>C</li>	
</ul>

## How it Works
<p>In its start state, both LEDs flash once per second.  Holding down one of the buttons tells the board to start counting how long to set the timer for.  After that, pressing the other button starts the countdown; the board deactivates its lights and waits for the same number of seconds that the first button was held down for.  At the end of the countdown, the board flashes its LEDs in an alternating pattern.</p>

## Design Decisions
<ul class="TechList">
	<li>I chose a very simple project, as there simply was not much time to develop anything complicated.</li>  
	<li>The "hold the button" input mechanism was selected to workaround not being able to find documentation on a function to make the board recognize individual button presses.</li>
	<li>I used flashing LEDs as a signalling mechanism, as they were the only output mechanism that I had available to me, due to my lack of other hardware components.</li>
</ul>


<br/>
<br/>
<br/>
<br/>
<br/>
