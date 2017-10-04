<a name="top"></a>
<a href="#lesson1">Lesson 1</a> | <a href="#lesson2">Lesson 2</a> | <a href="#lesson3">Lesson 3</a>

#HTML/CSS Basics for Designers
<a name="lesson3"></a>
###LESSON 3: More about CSS

-----

### Lesson 3 Topics

1. What's the "cascade"?
2. Applying selectors to HTML
3. Combining selectors
4. Common CSS Property Values
5. Type on the web
6. Font-properties

	
### 1) What's the "cascade"?
- Within CSS, all styles cascade from the top of a style sheet to the bottom, allowing different styles to be added or overwritten as the style sheet progresses.
- They can cascade across multiple selectors

		p {
  			background: orange;
  			font-size: 24px;
		}
		p {
		  background: green;
		}
		
- They can also cascade within individual selectors

			p {
			  background: orange;
			  background: green;
			}

- They can also cascade from file to file (handy when using a reset, for example)

	      <link rel="stylesheet" href="library/reset.css">
	      <link rel="stylesheet" href="library/style.css">


### 2) Applying selectors to HTML

- This is basic HTML and CSS interaction, but in the HTML, you can take a block of content and give it a selector. In the CSS, you define what that selector does and looks like. So, here you have a `<div>` called "hotdog". In the CSS, we tell it to give that `<div>` with the class "hotdog" a background color of brown:

				<!--HTML-->
				<div class="hotdog">
				  <p>...</p>
				</div>
				
				<!--CSS-->
				.hotdog {
				  background: brown;
				}

### 3) Applying selectors to HTML
- You can also combine selectors to more specifically target elements. Here we want all of the `<p>` tags to be brown except the one with the `.mustard` class. We can specifically target that single `<p>` element:
				
				<!--HTML-->
				<div class="hotdog">
				  <p>...</p>
				  <p>...</p>
				  <p class="mustard">...</p>
				</div>
				
				<!--CSS-->
				.hotdog p {
				  background: brown;
				}
				.hotdog p.mustard {
				  background: yellow;
				}
- You can layer styles as well by separating them with a space. Example might be a menu with a active menu item:

				<!-- HTML-->
				<ul>
				  <li class="menu-item">...</li>
				  <li class="menu-item">...</li>
				  <li class="menu-item active-menu-item">...</li>
				</ul>
				
				<!--CSS-->
				.menu-item {
				  color: blue;
				  width: 30px;
				  font-size: 1em;
				}
				
				.active-menu-item {
				  color: red;
				}


### 4) Common CSS Property Values


- Colors
	- Keyword colors (pretty old skool)
		- Color names like: red, blue, maroon, silver, purple
		- These are great for quick testing
	- Hex colors
		- Most common - there are 16.7 million of them!
		- formatted like: `#123456` or `#0051ba`
		- Shorthand: Six-character hexadecimal values may be written as three-character hexadecimal values when the red, green, and blue color channels each contain a repeating character
			-  for repeated numbers: `#111` = `#111111` or `#345` = `#334455`
	- RGB(A)
		- Includes RGB values as well as an alpha channel
			- `rgb(128, 0, 0)`
			- `rgba(128, 0, 0, .25)`
	- HSL(A)
		- Newest specification in CSS - not as well supported
		- Hue, Saturation, Lightness
		- `hsl(0, 100%, 25%)`
		- `hsla(60, 100%, 50%, 1)`

- Lengths
	- Pixels
		- 1/96th of an inch
		- Common standard of digital measurement
		- Useful for type and layouts
	- Percentages
		- Percentage lengths are defined in relation to the length of another object
			- For example, to set the width of an element to 50%, we have to know the width of its parent element, the element it is nested within, and then identify 50% of the parent element’s width.
		- Great for layout use
	- Em
		- length is calculated based on an element’s font size
		- Great for typography on the web
		- Typically `1em` = `16px`, I believe, but it easily changed by setting the body font size.
		- That said, don't worry about size as much. 
			- `1em` is a good starting point. Too big? Try `0.9em`. Too small? Try `1.2 em`. Play with it until you find what works.
		

### 6) Type on the web
- Has really evolved in the past 5 years, especially with the invention of TypeKit, Google Fonts, typography.com.
- There are many more options, but don't forget about the lowest common denominator.
	-  Basic rule of type (in my mind) - just because you *can* doesn't always mean you *should*
- Consider font stacks:
	- They list fonts as well as what they degrade to if they aren't available
	- Example: `font-family: 'Gotham Condensed', 'Arial Narrow', Arial, sans-serif;`



### 6) Font Properties
<https://www.w3schools.com/css/css_text.asp>

<table>
  <tr>
    <th style="width:20%">Property</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_color.asp">color</a></td>
    <td>Sets the color of text</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_direction.asp">direction</a></td>
    <td>Specifies the text direction/writing direction</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_letter-spacing.asp">letter-spacing</a></td>
    <td>Increases or decreases the space between characters in a text</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_dim_line-height.asp">line-height</a></td>
    <td>Sets the line height</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_text-align.asp">text-align</a></td>
    <td>Specifies the horizontal alignment of text</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_text-decoration.asp">text-decoration</a></td>
    <td>Specifies the decoration added to text</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_text-indent.asp">text-indent</a></td>
    <td>Specifies the indentation of the first line in a text-block</td>
  </tr>
  <tr>
    <td><a href="/cssref/css3_pr_text-shadow.asp">text-shadow</a></td>
    <td>Specifies the shadow effect added to text</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_text-transform.asp">text-transform</a></td>
    <td>Controls the capitalization of text</td>
  </tr>
  <tr>
    <td><a href="/cssref/css3_pr_text-overflow.asp">text-overflow</a></td>
    <td>Specifies how overflowed content that is not displayed should be signaled to the user</td>
  </tr>

  <tr>
    <td><a href="/cssref/pr_pos_vertical-align.asp">vertical-align</a></td>
    <td>Sets the vertical alignment of an element</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_white-space.asp">white-space</a></td>
    <td>Specifies how white-space inside an element is handled</td>
  </tr>
  <tr>
    <td><a href="/cssref/pr_text_word-spacing.asp">word-spacing</a></td>
    <td>Increases or decreases the space between words in a text</td>
  </tr>
</table>

####Pretty examples of web type
<http://www.awwwards.com/websites/typography/>


###<a href="#top">TO TOP</a>