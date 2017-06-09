# PDF Rulefinder

[Back to My Projects Page](projects.html)

## What Technologies Were Used?

- Node.js
- JavaScript
- JQuery
- MongoDB
- pdf-text-extract
- Express.js
- serve-static

## How it Works

When started with the `--refresh-db` flag, the program uses pdf-text-extract to extract text from all of the PDF files in a configured directory.  Upon the asynchronous extraction of the text of each PDF, it inserts the data into an entry for that book in MongoDB.  It then proceeds to operate as if the flag had not been used.

When starting normally, the program serves up a REST API, as well as a static web page in a public directory.  The web page uses JQuery to make calls to the REST API in order to get data, such as the available books and the most likely results from a given search.

The REST API serves up two main calls.  The first retrieves the list of available books in the configured directory, while the second retrieves search data.  

When search is invoked, the system uses MongoDB to retrieve the text for each selected book for the search, then proceeds to rank each page in that book in terms of how many keywords matched the search string.  After retrieving the top-ranked pages in each book, the search function compiles an ordered list of the winning pages in each book in the search list and returns that.  Conceptually, the search behaves similarly to a MapReduce job, though it lacks the parallelism of one.  

## The Story Behind the Project

Having completed my Node.js-based [dice roller](dice-rollers.html), it was time to begin work on a non-trivial project.  As I was still interested in producing a toolset for tabletop game masters, I started considering the technical aspects of producing a map-generator.  

Just before I was ready to begin working on the project, I got into a debate with a friend about the details of a monster in the D&D 3.5 Monster Manual.  As I went to look up information, I discovered a publically-accessible map generator and realized that I would be find more use in working on a utility that was less likely to already have been implmented.

Ultimately, I opted to work on a search utility for rulebooks, as opposed to re-inventing the map-generation wheel.  That said, I may end up making my own eventually, so that I can integrate it with this tool.




