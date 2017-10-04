<a name="top"></a>

#HTML/CSS Basics for Designers

<a name="lesson1"></a>
###LESSON 1: Getting familiar with HTML & CSS

--------

### Lesson 1 Topics

1. Working locally
	- Setting up files/folders/servers
2. What is HTML?
3. What is CSS?
4. Things to keep in mind

### 1) Working locally

- Software
	- Atom/Text wrangler - Free HTML editors
		- <https://atom.io/>
		- <http://www.barebones.com/products/TextWrangler/> (near end of life)
	- MAMP
		- Only needed for server processing needs
		- <https://www.mamp.info/en/>
	- CyberDuck (FTP client)
		- <https://cyberduck.io/>
- Setting up your folders

	```
	- index.html
		- images/
		- library/css
			- layout/css/reset.css
			- layout/css/style.css
		- library/js
	```
- How do servers work anyway?
	- Domain name points to a server
	- When someone accesses a URL (domain name), it goes to the server and pulls up that file to display in your browser.
	- If it's using a CMS, for example, the server will run some code to pull together various pieces of content before it is displayed - kind of like building the site on the fly.

- Give a server a try
	- KU offers some web space for personal use
	- It's an old carryover from years ago, but it's still live
		- <https://myidentity.ku.edu/services/PersonalWebSpace>


### 2) What is HTML?
*(See reference example A)*

- HTML
	- It's a programming language that lets you markup the content on a page to give it structure. It's a way to organize content, create links, and embed images.
	- All tags should be in lowercase (older code used uppercase).
	- Elements
		- Elements are designators that define the structure and content of objects within a page. They have limited styling capabilities like `strong`, `em`, 
		- Examples: `a`, `div`, `span`, `h1-h6`, `p`
		- Self-closing elements: `<br>`, `<hr>`, `<img>`, `<meta>`
	- Tags
		- Tags most commonly occur in pairs of opening and closing tags.
		- Example: `<a>...</a>`, or `<div>...</div>`
	- Attributes
		- Attributes are properties used to provide additional information about an element.
		- In the example: `<a href="http://www.ku.edu" class="home">KU Homepage</a>`, `href="http://www.ku.edu"` and `class="home"` are attributes.
	- Setting up the document structure (*see reference example A*)
	
 		```
		<!DOCTYPE html>
		<html lang="en">
		  <head>
		    <meta charset="utf-8">
		    <title>Example A</title>
		    <link rel="stylesheet" href="library/reset.css">
		    <link rel="stylesheet" href="library/style.css">
		  </head>
		  <body>
		  	<div>
		   	 <!-- Content goes here -->
		   	</div>
		  </body>
		</html>
		```
	

### 3) What is CSS?

![CSS Syntax Outline](images/css-syntax-outline.png)

- CSS (Cascading Style Sheets) is a way to apply styling and design to HTML code. If HTML is content, CSS is design. Keeping them separate makes sure that each file serves it's own function.
- Selectors
	- Type Selectors
		- Type selectors target elements by their element type (`p`, `h1-h6`, `li`, etc).
	- Class Selectors
		- 	Class selectors allow us to select an element based on the element’s class attribute value. Class selectors are a little more specific than type selectors, as they select a particular group of elements rather than all elements of one type.

		-	Class selectors allow us to **apply the same styles to different elements at once** by using the same class attribute value across multiple elements.

		-	Within CSS, classes are denoted by a leading period, `.`, followed by the class attribute value. Here the class selector will select any element containing the class attribute value of `awesome`.
			
			```
			CSS
			.awesome { ... }
			      
			HTML
			<div class="awesome">...</div>
			<p class="awesome">...</p>
			```
	- ID selectors
		- 	ID selectors are even more precise than class selectors, as **they target only one unique element at a time**. Just as class selectors use an element’s class attribute value as the selector, ID selectors use an element’s id attribute value as a selector.

		-	Regardless of which type of element they appear on, id attribute values can only be used once per page. If used they should be reserved for significant elements.

		-	Within CSS, ID selectors are denoted by a leading hash sign, `#`, followed by the id attribute value. Here the ID selector will only select the element containing the id attribute value of `jayhawk`.
			
			```
			CSS
			#jayhawk { ... }
			              
			HTML
			<div id="jayhawk">...</div>
			```
- Including a CSS file in your HTML document
	- In the head of the document, you'll want to link to the stylesheet:
			```
			<head>
			  <link rel="stylesheet" href="style.css">
			</head>
			```
- CSS Resets
	- Why do you need one?
		- Browsers are infamously incompatible.
		- The goal of a reset stylesheet is to reduce browser inconsistencies in things like default line heights, margins and font sizes of headings, etc.
		- [Eric Meyer's reset is a good and widely used one](http://meyerweb.com/eric/tools/css/reset/)

### 4) Things to keep in mind
- **Clean code will make life SO much easier!**
	- It will make it easier for you to go back to later on **OR** for someone else to go in and read what you're doing.
	- Don't be afraid to add comments.
		- In HTML, you write it: `<!-- Comment Goes Here -->`
		- In CSS, you write it: `/* Comment Goes Here */`
		- Both apply to single and multiple lines
		
			```
				<!-- Here's a comment
				that spans two lines -->
				
				/* Here's a comment that
				spans two lines */
			```
- Naming of CSS selectors are completely up to you - however, make sure they make sense!
	- For example, you can get cute and call the sidebar selector `puppy_dogs`, but you'd be better off to call it `sidebar` or better yet `right_sidebar`.


--
### References
Great overall tutorial:
<http://learn.shayhowe.com/html-css/>

--------

###<a href="#top">TO TOP</a>