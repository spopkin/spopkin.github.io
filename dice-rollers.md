# ASM Roller and JavaScript Dice Roller

[Back to My Projects Page](projects.html)

## What Technologies Were Used?

ASM Roller
- x86 assembly
- Linux system calls

dice-roller.js
- Node.js
- JavaScript


## How They Work

The assembly-based dice roller is an i686 assembly program written for Linux.  It is compiled using NASM and Make.

It takes command line arguments to specify the number of dice to roll and how many sides that each die should have, then opens /dev/urandom to read in an appropriate number of random bytes.  After reading in enough bytes, it transforms them into readable integers of the appropriate range before printing them to the command line.

The JavaScript version uses Node.js instead of x86 assembly, but has similar usage.  When called it takes the same parameters and uses Math.random to get values that it can print to the command line.


## The Story Behind the Project

After taking a class on assembly programming as a part of my required coursework, I decided that I was interested in playing with assembly a little bit more.  As such, I wanted to work on a simple application that would be manageable, while also being something that I could concieve a potential use for.  

Having played D&D in high school, I considered the possibility of making tools that would be useful for game masters to use to simplify the process of building complex game worlds and running games based on them.  While most of the tools that I had in mind to create would have been outside of the complexity scope that I had envisioned, a simple dice-rolling program was not.

Given my newfound inspiration, I successfully implemented the dice roller, then debated on what tools and technologies to use for the remaining utilities that I intended to create.

After a busy period of coursework in which I had not had time to implement any further personal projects, I eventually forgot that I had created this program.

Eventually, when deciding on personal projects to do later on, I re-encountered the program on my GitHub and ultimately opted to resume development.  This time, I decided to use a more maintainable set of technologies that seemed like they would be better for more quickly developing the programs, as x86 assembly would have been unmaintainable for some of the more complicated ones that I had in mind.  Ultimately, I elected to use JavaScript due to its cross-platform support, ease of quick development, and increasing prevalence on job applications.  As none of my project ideas seemed to require any particular libraries or abnormal dependencies to work, I deemed it appropriate for the job and began working with Node.js to re-implment the dice-roller in JavaScript as a warmup program.
