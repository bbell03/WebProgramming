# Thursday, January 16th: Course Introduction
* Why the web?  Why are you here?
* Motivation 1, the first web page (1992): http://info.cern.ch/hypertext/WWW/TheProject.html
* Motivation 1A: http://line-mode.cern.ch/www/hypertext/WWW/TheProject.html
* Motivation 2: http://www.dolekemp96.org/
* Motivation 3: https://archive.org/
* What this course is not...
* What this course is...
  * Why I still like teaching this class...
* Administrativa:
  1. The bad news: course is closed, wait-list
  2. No final exam for this class, book travel now
  3. Lab 1 up
* How two computers talk to each other: basic networking
* The Internet vs the World Wide Web

# Tuesday, January 22nd: HTTP
* PSA on sexual harassment
* Last class: the big ideas?
* Recall telephone conversation example
* Telephone extension numbers
* So what is the web?
* Two special computers: web server and web client
* URLs:
  `protocol://domain/<any directories here>/<filename>`
* The big idea of HTTP, how the web works: request-response, similar to Q&A
* Examining HTTP requests and responses on Reddit...
* HTTP commands: GET and POST
  - GET: Download data
  - POST: Upload data, send data to web server
  
# Thursday, January 24th: HTML
* Last class: recall how HTTP works
* Recall question: if no port number is provided, the default port number to connect to on web server is...?
* Recall question: what HTTP command is executed when entering URL address?
* Q: How to browse web without web browser?
* Demo: Web server
* Recall question: if no file is provided in URL, the file with what name is generally served by default?
* Take a look at the HTML
* What is markup?
  - The paragraph analogy
* Motivation: writing
* Block vs. inline elements
* Attributes
* Image --a special tag...
* Anchors
* Absolute vs relative URLs
* W3C validator

# Tuesday, January 29th: Revision Control with Git
* Recall: block elements, absolute vs relative sources, W3C validator, example
* What's wrong with the HTML?
* What I've noticed in the past: many connecting to Tufts CS to do work via SSH, questions on submitting assignments and labs in this class, how to upload web pages to a server
* The nightmare scenario that illustrates the need for revision control: in the past...
* What if I need to hire developers to work on different pieces of a projet?
* Why revision control? Keep track of changes, document changes
* Why Git? Speed, no dependency of a remote server (unlike Subversion)
* Why GitHub for repositories? Network effect, communications
* Example with our course website
* IMPORTANT: you are not expected to master Git by the end of this course.  The reality, even for the most seasoned people: https://twitter.com/ErrataRob/status/707327952158121984

# Thursday, January 31st: Cascading Style Sheets (CSS)
* Why do you want to separate style?
* One CSS _rule_ is made up of _selectors_ and _declarations_. A declaration is a _property-value_ pair.
  - You really want to refer to a CSS cheat sheet!
* Three types of selectors: HTML tag names, ID, class
  - ID: should only be used once; starts with "#"
  - class: can be used many times; start with "."
  - Mixing IDs and classes is confusing, generally not a good idea.
  - "id" and "class" attribute exist for all HTML elements
  - Generic block HTML element: div
  - Generic inline HTML element: span
* Box model for HTML body elements
* The "cascading" in "cascading style sheet"
  - What if there is more than one style specified for an HTML element?

# Tuesday, February 5th: Responsive Design
* Last class: CSS
* Why CSS?  What do they give you?
* Recall: id vs class
* Recall: what is cascading?
* Question: _how do you build a web browser?_
* Loading additional stylesheets
* Today: mobile
* Take out your phone or mobile device.  Go to...
* How mobile web browsers work: render pages in a virtual window (i.e., the viewport), usually wider than the screen, so they don't need to squeeze every page layout into a tiny window. Users can pan and zoom to see different areas of the page.  That is, a mobile browser it will assume that you are viewing a desktop experience and that you want to see all of it.
* `<meta name="viewport" content="width=device-width; initial-scale=1.0; maximum-scale=1.0; user-scalable=0;" />` => your layout will be displayed properly at 1:1 scale.  No zooming will be applied.
* So can I have a different stylesheets for different screen sizes and devices?
  - http://broadcast.oreilly.com/2010/04/using-css-media-queries-ipad.html
  - `<link rel="stylesheet" media="all and (max-device-width: 480px)" href="iphone.css">`
  - `<link rel="stylesheet" media="all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation:portrait)" href="ipad-portrait.css">`
  - `<link rel="stylesheet" media="all and (min-device-width: 481px) and (max-device-width: 1024px) and (orientation:landscape)" href="ipad-landscape.css">`
  - `<link rel="stylesheet" media="all and (min-device-width: 1025px)" href="ipad-landscape.css">`
* Can I have different rules in a CSS for different screen sizes (e.g., widths)?
* Gmail: http://googleappsdeveloper.blogspot.com/2016/09/your-emails-optimized-for-every-screen-with-responsive-design.html
* Your next lab
* Why this technique?

# Thursday, February 7th: JavaScript
* File permissions
* So far, we have covered quite a bit: HTTP, HTML, CSS, Git
* What are the problems and limitations with just HTML and CSS?
* HTTP: stateless protocol, no memory of previous requests
* In the early 90s, "Netscape quickly realized that the Web needed to become more dynamic. Even if you simply wanted to check that users entered correct values in a form, you needed to send the data to the server in order to give feedback." http://speakingjs.com/es5/ch04.html
* Our focus is still on the client-side
* Variables: dynamic typing but will be one of the following: number, string, array, object, boolean
  - Three states of a variable: (1) not set yet (undefined), (2)set to nothing (null), (3) set to a valid value
* Operations: "+" is interesting
* Lists (a.k.a., arrays)
* _(Almost)_ everything in JavaScript is an object_ https://stackoverflow.com/questions/9108925/how-is-almost-everything-in-javascript-an-object
* Okay, but how do I use JavaScript in an HTML page?  Or how do I dynamically modify a loaded HTML page using JavaScript?

# Tuesday, February 12th: Document Object Model (DOM)
* Last class: JavaScript data and data structures (lists and dictionaries)
* The big idea: using JavaScript to dynamically modify HTML content _after it is loaded_.  Yes, you can mix HTML and JavaScript
* Today: the "var" keyword, using JavaScript in an HTML page
* The document object: a JavaScript object that contains the entire structure of an HTML page after it is loaded, in tree-like format (thus, known as the Document Object Model tree).  Example of a DOM tree: https://developer.mozilla.org/en-US/docs/Using_the_W3C_DOM_Level_1_Core
* Example 1: Fiddle https://jsfiddle.net/mchow01/0wga8wLp/3/?utm_source=website&utm_medium=embed&utm_campaign=0wga8wLp
* Example 2: Highlighting paragraphs in an HTML document

# Thursday, February 14th: Functions in JavaScript
* Your Assignment 2
* Recall: almost everything in JavaScript is a/an ______
* Too many built-in JavaScript objects to name: string, Date, Math
* Special object in JavaScript: the associative array a.k.a., dictionary a.k.a., hash a.k.a., finite map
* So what about functions?
* Function arguments: (1) too many: extras ignored, (2) too few: remainders get an undefined value
* Who is in COMP 105 currently or have taken COMP 105?
* What if I told you functions can be used as values to variables? Functions as arguments to functions? That's what it means by functions as first-class!
* Consider example at http://www.joelonsoftware.com/items/2006/08/01.html
* Recall Algebra: function composition
* Why is this a powerful idea?
  - Reduce repetitive code
  - More reusable and scalable code
  - "Object Oriented Programming" in JavaScript
  - Example: `apply` https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply
* Example: https://jsfiddle.net/mchow01/72j6knum/1/
* Is this idea that important in JavaScript? Yes, not only in JavaScript but in many languages and frameworks as well
  - Events
  - Callbacks (e.g., working with the GPS)
  - Asynchronous communications (e.g., downloading data from the web within a running app)
* A powerful idea: update the HTML based on events, combine DOM + first class functions
* Example: Double Rainbow
* Your next lab
* Next time: even more powerful idea: update the HTML with data from a web server