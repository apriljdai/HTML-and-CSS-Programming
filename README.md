HTML-and-CSS-Programming
========================
Part I: HTML 
1.	HTML Elements
	documents are made up by elements. 
	HTML elements is everything from the start tag to the end tag. 
	HTML elements can be nested(elements contain elements)
	the <html> element defines the whole document, the element content is another HTML element(e.g. <body> element)
	HTML elements with no content are called empty elements
	<br> is an empty element without a clocing tag, which defines a line break. It could be closed in <br />

2.	HTML Attributes
	provide additional information about an element.
	attributes are always specified in the start tag, comes in name/value pairs: name="value"
	-- the lang attribute
	-- the title attribute: provides addition "tool-tip" info
		<p> element has an attribute. e.g. <p title="About sth">
		when move the mouse over the element, the title will be displayed as a tooltip
	-- the href attribute(link): provides address info for links
	-- the size attribute(image, src, width and height are all provied as attributes)
	-- the alt attribute: provides text for screen readers
		specifies an alternative text to be used, when an HTML element cannot be displayed.
		the value of the attribute can be read by "screen reader"
	(always double quote attribute values, always use lowercase)
	other attributes
	-- disabled: an input element should be disabled
	-- id: a unique id for an element
	-- style: an inline CSS style for an element
	-- value: the text content for an input element

3.	HTML Headings
	defined with the <h1> to <h6> tags
	<h1> defines the most important heading, <h6> defines the least important heading
	Don't use headings to make text big or bold
	search engines use your headings to index the structure and content to your web pages
	user skim your pages by its headings
	it's important to use headings to show the document structure
	h1 headings should be main headings, followed by h2 headings, and so on.
	
	<hr> tag creates a horizontal line in an HTML page.
	<meta> element is also meta data, used to define the character set, and other info about the HTML document

4.	HTML Paragraphs
	HTML documents are divided into paragraphs
	Browsers automatically add an empty line before and after a paragraph
	HTML Display: cannot be sure how HTML will be displayed(size of screens, and resized windows will create different results)
	can NOT change the output by adding extra spaces or extra lines in the HTML code(THe browser will remove extra spaces and extra lines when the page is displayed)
	any number of spaces and new lines count as only one space
	<br> element defines a line break, it is en empty HTML element, has no end tag
	<pre> element defines a block of pre-formatted text, with structured spaces and lines.(if you need whole paragraph as pre-fomatted, just use <pre> instead of <p>)

5.	HTML Styling
	HTML element has a defalut style(background color is white, text color is black, text-size is 12px), change the default style of an HTML element, can be done with the style attribute.
	<body style="background-color:lightgrey"> changes the default background color from white to lightgrey(not valid in HTML5)
	<h1 style="color:blue"> defines the text color to be used for an HTML element
	(style="property:value" is HTML style attribute syntax, property/value is a CSS property/value)
	<h1 style="font-family:verdana"> font-family defines the font to be used for an HTML element(not valid in HTML5)
	<h1 style="font-size:300%"> font-size defines the text size
	<h1 style="text-align:center"> text-align defines the horizontal text alignment(not valid in HTML5)

6.	HTML Text Formatting
	special elements, for defining text with a special meaning.
	-- bold text <b> 
	-- important text <strong>(in semantic importance), means the text is "important"
	--italic text <i> 
	-- emphasized text <em> (emphasized in semantic importance), means the text is "important"
	-- marked text <mark> (highlighted text)
	-- small text <small> 
	-- deleted text <del>
	-- inserted text <ins>
	-- subscripts <sub>
	-- superscripts <sup>

7.	HTML Quatation and Citation
	1) short quatation <q>
	2) long quatation <blockquote> (usually indent elements)
	<abbr title="World Health Organization">WHO</abbr> defines an abbreviation, can give useful info to browsers, translation system and search-engines
	<dfn title=>"World Health Organization">WHO</dfn>  defines the definition of a term or an abbreviation
		- if the title attribute is present, it defines the term
		- <dfn><abbr title="World Health Organization">WHO</abbr></dfn>, title defines the term
		- <dfn>WHO</dfn> World Health Organization... text content is the term, <p> contains the definition
	<address> defines contact info (author/owner) of a document, usually displayed in italic.
	<cite> defines the title of a work, usually displays in italic
	<bdo> bi-directional override, text be written from right to left

8.	HTML Computer Code Formatting
	normally HTML use variable letter size and variable letter spacing (not for computer code)
	-- <kbd> keyboard formatting
	-- <samp> computer output sample
	-- <code> programming code sample (does NOT preserve extra whitespace and line-breaks, use<pre> to fix)
	-- <var> mathematical variable

9.	HTML Comment Tag
	<!-- Your comments here -->
	comments are not displayed by the browser
	-- help document your HTML
	-- place notifications and reminders in the HTML
	-- great for debugging HTML

10.	HTML Style with CSS (Cascading Style Sheets)
	Styling can be added to HTML element in 3 ways:
	-- Inline: use a style attribute 
			   useful for applying a unique style to a single HTML element
	-- Internal: use a <style> element in the HTML <head> section
				 used to define a common style for all HTML elements on a page
	-- External: use one or more external CSS files
				 ideal when the style is applied to many pages, change the look of an entire site by changing one file
				 defined in the <head> secion of an HTML page, in the <link> element
				 eg. <link rel="stylesheet" href="styles.css">

	1)  CSS Syntax:
		element { property: value ; property:value }
		element: an HTML element name
		multiple styles are separated with semicolon
	2)	CSS Fonts 
		- color: defines the text color to be used 
		- font-family: defines the font to be used (not valid in HTML5)
		- font-size: defines the text size to be used (not valid in HTML5)
		eg. h1 {
				color: blue;
				font-family: verdana;
				font-size: 300%;
			}
	3)	CSS Box Model
		Every visible HTML element has a box around it, even if cannot see it.
		- border: defines a visible border around an HTML element
		- padding: defines a padding(space) inside the border
		- margin: defines a margin(space) outside the border
		eg. p {
				border: 1px solid blue;
				padding: 10px;
				margin: 30px;
			}
		(px: define sizes in screen pixels)

	CSS styles define an equal style for all equal elements. To define a special style for a special element, add an id attribute to the element:
	eg.	<p id="p01">paragraph content</p>
	Then define the special style element:
	p#p01 {
		color:blue;
	}
	To define for a special type(class) of element:
	eg.	<p class="error">one special element in a group</p>
		<p class="error">another special element in a group</p>
		p.error{
			color: red;
		}

	NOTE: 
		- id: address single elements
		- class: address group of elements

11.	HTML Links
	Links allow users to click their way from page to page
	HTML links are hyperlinks
	A hyperlink is an element, a text or an image that you can click on, and jump to another document

	links are defined with <a> tag:
	eg.	<a href="url">link text</a>
	href attribute: specifies the destination address
	link text: the visible part (can also be HTML image or other HTML element)

	-- local links: specified with a relative URL without the full web address(only the last)
	eg. <a href="http://wwww.W3Schools.com/html/html_images.asp">HTML Image</a> could be written as
		<a href="html_images.asp">HTML Image</a> 
	Default links colors and icons
	- unvisited link is underlined and blue
	- visited link is underlined and purple
	- active link is underlined and red (active means when the mouse is on it)

	<target> attribute: specifes where to open the linked document
	eg. <a href="http://www.W3Schools.com/" target="_blank">Visit W3Schools</a>
	- _blank: opens the linked document in a new window or tab
	- _self: opens the linked document in the same frame as it was clicked(default)
	-_parent: opens the linked document in the parent frame
	-_top: opens the linked document in the full body of the window(use to break out of the frame)
	framename: opens the linked document in a named frame

	image as link
	eg. <a href="html_images.asp">
		<img src="smiley.gif" alt="HTML tutorial" style="width:42px; height:42px; border: 0">
		</a>

	id attribute
	add an id attribute to an <a> element->create a link to the <a> element
	eg. <a id="tips">useful tips section</a>
		<a href="#tips">visit the useful tips section</a>

12.	HTML images
	Always specify image size, the page will flicker while the image loads if the size is unknown
	Images are defined with the <img> tag, the tag is empty, contains attributes only
	eg. <img src="url" alt="some_text">
	-- 	src attribute 
		defindes the image file name
	--	alt attribute (required!!)
		specifies an alternate text for the image, if it cannot be displayed.
		the value of the alt attribute should describe the image in words

	HTML screen readers are software programs that can read what is displayed on a screen. It can "reproduce" HTML as text-to-speech, sound icons, or braille output (can read alt attribute)

	-- 	size
		- can use style attribute to specify the width and height(values are specified in pixels with px)
		- can use width and height attributes(values are specified in pixels without px)
		Prefer to use style attribute to avoid the styles sheets from changing the default size

	- If no specified, the browser expects to find the image in the same folder as the web page.
	  To store images in a sub-folder, and refer to the folder in the image name
	  eg. <img src="/images/html5.gif" alt="HTML Icon" style="width:128px; height:128px">
	- If a browser cannot find the image, it will display a broken link icon
	  <img src="wrongname.gif" alt="HTML Icon" style="width:128px;height:128px">
	- can also access image from any web address in the World
	- can allow animated images (GIF)

	-- 	image maps (with clickable areas)
		- usemap attribute: point to an image map
		<img src="planets.gif" alt="Planets" usemap="#planetmap" style="width:145px;height:126px">
		<map name="planetmap">
			<area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm">
			<area shape="circle" coords="90,85,3" alt="Mercury" href="mercur.htm">
			<area shape="circle" coords="124,58,8" alt="Venus" href="venus.htm">
		</map>

	-- 	image float
		float the image to the left or right of a paragraph
		<p>
			<img src="smiley.gif" alt="Smiley face" style="float:left; width:42px; height:42px">
		</p>

13.	HTML Tables
	--	Tables are defined with the <table> tag.
	-- 	Tables are divided into table rows with the <tr> tag.
	-- 	Table rows are devided into table data with the <td> tag.(contains all HTML elements: text, image, list, table, etc.)
	-- 	A table row can also be divided into table headings with the <th> tag.

	--	border 
	1) 	border attribute
		<table border="1" style="width:100%">
			<tr>
				<!-- default display table headings as bold and centered -->
				<th>First Name</th>
				<th>Last Name</th>
				<th>Age</th>
			</tr>
			<tr>
				<td>Jill</td>
				<td>Smith</td>
				<td>50</td>
			</tr>
			<tr>
				<td>Eve</td>
				<td>Jackson</td>
				<td>94</td>
			</tr>
		</table>
	2)	CSS border property (define both table and table cells)
		table, th, td {
			border: 1px solid blue;
			<!-- make the borders collapse into one border -->
			border-collapse: collapse;
		}
	--  cell padding
		specifies the space between the cell content and its borders
		the table cells will be displayed without padding if not specifying it
		th, td {
			padding: 5px;
		}
	-- 	table heading
		left-align the table headings, use the CSS text-align property
		th {
			text-align: left;
		}
	-- 	border spacing
		specifies the space between the cells, use the CSS border-spacing property
		border-spacing has no effect if has border-collapse!!
		table {
			border-spacing: 5px;
		}
	--  rowspan/colspan attribute
		make a cell span more than one row/column
		<th rowspan="2">
	--  caption tag
		<table style="width:100%">
			<caption>People Info</caption>
			....
		</table>
	--  different styles for different Tables
		the style in the <head> section defines a style for all table in a page.
		- id attribute 
		  define a special style for a special table
		  <table id="t01">
		  	...
		  </table>

		  <style>
		  	table#t01 {
		  		width: 100%;
		  		background-color: #f1f1c1;
		  	}
		  	table#t01 tr:nth-child(even) {
		  		background-color: #eee;
		  	}
		  	table#t01 tr:nth-child(odd) {
		  		background-color: #fff;
		  	}
		  	table#t01 th {
		  		color: blue;
		  		background-color: lightblue;
		  	}

14.	HTML List 
	HTML can have unordered/ordered/description list 
	--  unordered list
		- unordered list starts with <ul> tag.
		- each list item starts with <li> tag.
		- the list items will be marked with bullets(small black circles)
		<ul>
			<li>Coffee</li>
			<li>Tea</li>
		</ul>
		- 	style attributes (not valid in HTML5 unordered list)
			define the style of the marker
			1) list-style-type:disc (marked with bullets, default)
			2) list-style-type:circle (marked with circles)
			3) list-style-type:square (marked with squares)
			4) list-style-type:none (not be marked)
	--  ordered list
		-	type attribute 
			define the type of the marker
			1) type="1" (the list items will be numbered with numbers, default)
			2) type="A" (the list item will be numbered with uppercase letters)
			3) type="a" (the list item will be numbered with lowercase letters)
			4) type="I" (the list item will be numbered with uppercase roman numbers)
			5) type="i" (the list item will be numbered with lowercase roman numbers)
			<ol type="1">
				<li>Coffee</li>
				<li>Tea</li>
			</ol>
	-- 	description list 
		a list of terms, with a description of each term
		- <dl> tag defines a description list
		- <dt> tag defines the term (name)
		- <dd> tag defines the data (description)
		<dl>
			<dt>Coffee</dt>
			<dd>- black hot drink </dd>
			<dt>Milk</dt>
			<dd>- white cold drink</dd>
		</dl>
	list can be nested (lists inside lists)
	--  horizontal list
		use id attribute
		<style>
		ul#menu li {
			display: inline;
		}
		</style>
		...
		<ul id="menu">
			...
		</ul>

15.	HTML Block Elements
	Most HTML elements are defined as block level elements or inline elements
	--  Block level elements
		normally start (and end) with a new line when displayed in a browser
		eg. <h1>, <p>, <ul>, <table>
	--  Inline elements
		normally displayed without line breaks
		eg. <b>, <td>, <a>, <img>

	--  HTML elements
		- 	<div>
			a block level element
			used as a container for other HTML elements
		-	<span>
			inline element
			used as a container for text
			<h1>My <span style="color:red">Important</span> Heading</h1>

16.	HTML Class
	Classing HTML elements makes it possible to define CSS styles for classes of elements
	--  Classing Block elements
		classing <div> elements, makes it possible to define equal styles for equal <div> elements
		eg. <div class="cities"> (can be used in multiple paragraphs)
	--  Classing Inline elements
		classing <span> elements makes it possible to design equal styles for equal <span> elements

17.	HTML Layouts
	--  using <div> elements
		<div> elements is often used as a layout tool because it can easily be positioned with CSS
	--  using HTML5 layout
		- header: defines a header for a document or a section (top)
		- nav: defines a container for navigation links (second top)
		- section: defines a section in a document (left)
		- article: defines an independent self-contained article (left)
		- aside: defines content aside from the content (right)
		- footer: defines a footer for a document or a section (bottom)
		- details: defines additional details
		- summary: defines a heading for the details elements
	--  using tables
		<table> element was not designed to be a layout tool (is to display tabular data)

18.	HTML RWD (Responsive Web Design)
	RWD delivers web pages in variable size
	RWD is a MUST for tablets and mobile devices
	-- 	using Bootstrap
		Bootstrap is the most popular HTML, CSS and JS framework for developing responsive webs
		Bootstrap helps you to develop sites that look nice at any size

19.	HTML Iframes
	used to display a web page within a web page
	<iframe src="URL"></iframe>
	--  set height and width
		use height and width attributes: specify the size
	-- 	remove the border
		frameborder attributes: specifies whether or not to display a border around
		"0" to remove the border
		<iframe src="demo_iframe.htm" frameborder="0"></iframe>
	--  used as the target frame for a link
		target attribute: refer to the name attribute of the iframe
		<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
		<p><a href="http://www.w3schools.com" target="iframe_a">W3Schools.com</a></p>

20.	HTML Color 
	-- 	color names
		140 color names are supported by all browsers (in the HTML5 and CSS3 color specifications)
		17 colors are from HTML, 123 colors are from the CSS
	-- 	color values
		- colors are displayed combing RED, GREEN, and BLUE light
		  colors are defined using a hex notation for RGB
		  the lowest value for each light source is 0(hex 00), the highest value is 255(hex FF)
		  hex value are written as # followed by either 3 or 6 hex characters
		  3 notations(#rgb) are automatically converted to 6 digits(#rrggbb)
		  <h1 style="background-color:#FF0000">
		  <h1 style="background-color:rgb(0,255,0)">
		  <h1 style="background-color:blue">	
		- shades of grey(from black to white)
		  #000 to #888 to #FFF(black to grey to white)
	--  color shades
		gray colors are displayed using an equal amount of power to all of the light sourses (rgb 3 values are equal)
	The combination of RGB gives a total of more than 16 million different colors to play with (256*256*256)
	The most modern monitors are capable of displaying at least 16384 different colors

21.	HTML JavaScripts
	JavaScripts make HTML pages more dynamic and interactive.
	-- 	<script> tag
		used to define a client-side script.
		either contains scripting statments or points to an external script file through the src attribute
		eg. <script>
				document.getElementById("demo").innerHTML = "Hello JavaScript!";
			</script>
			write Hello JavaScript into an HTML element with id="demo"
	-- 	<noscript> tag
		used to provide an alternate content for users that have disabled scripts in their browser or have a browser that doesn't support client-side scripting.
		contains all the elements that you can find inside the <body> element of a normal HTML page
		the content inside it will only be displayed if scripts are not supported, or are disabled in the user's browser.
		eg. <noscript>Sorry, your browser does not support JavaScript!</noscript>

22.	HTML Head
	--  <head> element
		a container for meta data(data about data)
		- HTML meta data 
		  data about the HTML document (metadata is not displayed)
		  typically define document title, styles, links, scripts, and other meta info
		  meta data tags:
		  1) <title>
		  2) <style>
	 	  3) <meta>
		  4) <link>
		  5) <script>
		  6) <base>
	--  omitting tags
		In HTML5, <html>, <body> and  <head> tag can be ommitted.
		<html> element is the document root. it is recommended place for specifying the page language (declaring a language is important for accessibility application and search engines)
		- omitting <html> and <body> can crash badly written DOM and XML software
		- omitting <head> can reduce the complexity of HTML
	--  <title> element
		defines the title of the document
		required in all HTML/XHTML documents
		- defines a title in the browser toolbar
		- providesa title for the page when it is added to favorites
		- displays a title for the page in search engine results
	--  <style> element
		used to define style info for an HTML document
		inside it you specify how HTML elements should render in a browser
	--  <link> element
		defines the page relationship to an external resource
		is most often used to link to stylesheets
	--  <meta> element
		used to specify page description, keywords, author, and other metadata
		used by browsers(display content), by search engines(keywords), and other web services
	--  <script> element 
		see above...
	--  <base> element
		specifies the base URL and base target for all relative URLs in a page
		eg. <base href="http://www.W3Schools.com/image/" target="_blank">

23.	HTML Entities
	- reserved characters in HTML must be replaced with character entities
	- characters, not present on your keyboard, can also be replaced by entities
	some characters are reserved in HTML (eg. < >, the browser might mix them with tags even you want present less than or greater than)
	character entities are used to display reserved characters in HTML
	character entity looks like:
	&entity_name; (advantage: easier to remember. disadvantage: may not support all entity names)
	or like:
	&#entity_number;
	--  diacritical mark
		a "glyph" added to a letter
		can appear both above and below a letter, inside a letter, and between two letters
		can be used in combination with alphanumeric numbers, to produce a character that is not present in the character set

24.	HTML Symbals
	Many mathematical, technical, and currency symbols are not present on a normal keyboard
	use an HTML entity name or number (decimal or hex reference) to add these symbols

25.	HTML Encoding(character set)
	--  ASCII
		the first character encoding standard (character set)
		it defines 127 different alphanumeric characters
		0 to 31 and 127 for control characters
		32 to 126 for letters, digits, and symbols
		does NOT use the values from 128 to 255
	--  ANSI
		the original windows character set
		it supported 256 different character codes
		identical to ASCII from 0 to 127
		128 to 159 for proprietary set of character
	--	UTF-8 (unicode)
		covers almost all of the characters and symbols in the world
		identical to ASCII from 0 to 127
		identical to ANSI from 160 to 255
		does NOT use value from 128 to 159
		continues from 256 with more than 10000 different characters
	To display an HTML page, a web browser must know the character set used in the page
	use <meta> tag to specify the character set:
	eg. <meta charset="UTF-8">

26.	HTML URL (Uniform Resource Locators)
	URL is another word for a web address
	URL can be composed of words, or an IP (Internet Protocol) address
	--  URL
		web browsers request pages from web servers by using a URL
		URL is used to address a document or other data on the web
		web address syntax rules:
		scheme://host.domain:port/path/filename
		- scheme: defines the type of internet service (most is http)
		  		  - http (hypertext transfer protocol): common web pages, not encrypted;
		  		  - https (secure hypertext transfer protocol): secure web pages, encrypted;
		  		  - ftp (file transfer protocol): downloading or uploading files;
		  		  - file: a file on your computer;
		- host: defines the domain host (default for http is www)
		- domain: defines the internet domain name (whaterver.com)
		- port: defines the port number at the host (default for http is 80)
		- path: defines the path at the server (if omitted: the root directory of the site)
		- filename: defines the name of a document or resource
	--  URL encoding
		URL can only be sent over the internet using the ASCII character set (since URLs often contain characters outside the ASCII set, the URL has to converted into ASCII)
		- converts characters into a format that can be transmitted over the internet
		- replaces non ASCII characters with a % followed by hex digits
		- cannot contain spaces, normally replaces a space with a plus(+) sign, or %20

27.	HTML &  XHTML(XML)
	- XHTML: extensible hypertext markup language
	- XHTML is almost identical to HTML
	- XHTML is stricter than HTML
	- XHTML is HTML defined as XML application
	- XHTML is supported by all major browsers
	--  Why XHTML
		XML is a markup language where document must be marked up correctly (well-formed)
		XHTML is combining the strengths of HTML and XML (avoid bad HTML)
		XHTML is HTML redesigned as XML
	--  Differences from HTML
		- document structure
		  XHTML DOCTYPE is mandatory (required)
		  the xmlns attributes in <html> is mandatory (<html xmlns="http://www.w3.org/1999/xhtml">)
		  <html>,<head>,<title> and <body> are mandatory
		- XHTML elements
		  must be properly nested
		  must always be closed (even for empty element, eg. <br />,<hr />,<img ... />)
		  must be in lowercase
		  must have one root element
		- XHTML attributes
		  must be in lowercase
		  values must be quoted (use "")
		  minimization is forbidden
	--  Convert from HTML to XHTML
		- add an XHTML <!DOCTYPE> to the first line of every page
		- add an xmlns attribute to the html element of every page
		- change all elements name to lowercase
		- change all empty elements
		- change all attribute names to lowercase
		- quote all attribute values

28.	HTML Forms
	<form> element is used to collect user input
		<form>
		.
		form elements
		.
		</form>
	form elements are different types of input elements, checkboxes, radio buttons, submit buttons, etc
	-- 	<input> element
		the most important form element
		has many variations, depending on the type attribute (eg. text, radio, submit)
		- text input
		  <input type="text"> 
		  defines a one-line input field for text input
		  the form itself is not visible, the fefault width of a text field is 20 characters
		  eg. <form>
		  	  First Name:<br>
		  	  <input type="text" name="firstname">
		  	  <br>
		  	  Last Name:<br>
		  	  <input type="text" name="lastname">
		  	  </form>
		- radio button input
		  <input type="radio">
		  defines a radio button, let the user select ONE of a limited number of choices
		  eg. <form>
		  	  <input type="radio" name="sex" value="male" checked>male
		  	  <br>
		  	  <input type="radio" name="sex" value="female">female
		  	  </form>
		- submit button input
		  <input type="submit">
		  defines a button for submitting a form to a form-handler
		  the form-handler is typically a server page with a script for processing input data
		  the form-handler is specified in the form's action attribute
		  eg. <form action="action_page.php">
		  	  First Name:<br>
		  	  <input type="text" name="firstname">
		  	  <br>
		  	  Last Name:<br>
		  	  <input type="text" name="lastname">
		  	  <br><br>
		  	  <input type="submit" value="Submit">
		  	  </form>
		  --  action attribute
		  	  defines the action to be performed when the form is submitted
		  	  the common way to submit a form to a server is by using a submit button
		  	  normally, the form is submitted to a web page on a web server
	--	<select> element
		defines a drop-down list
		eg. <form action="action_page.php">
			<select name="cars">
			<option value="volvo">Volvo</option>
			<option value="audi">Audi</option>
			<option value="honda">Honda</option>
			<option value="bmw">BMW</option>
			</select>
			<br><br>
			<input type="submit">
			</form>
		- <option> element
		  defines the options to select
		  normally show the first item as selected
		  you can add a selected attribute to define a predefined option
		  eg. <option value="audi" selected>Audi</option>
	-- 	<textarea> element
		defines a multi-line input field (text area)
		eg. <form action="action_page.php">
			<textarea name="message" rows="10" cols="30">
			...
			</textarea>
			<br><br>
			<input type="submit">
			</form>
	-- 	<button> element
		defines a clickable button
		eg.	<button type="button" onclick="alert('Hello World!')">Click Me</button>

	HTML5 Form Elements
	--	<datalist> element
		specifies a list of pre-defined options for an <input> element
		user will see a drop-down list of pre-defined options as they input data
		- list attribute
		  an attribute of the <input> element
		  must refer to the id attribute of the <datalist> element
		eg.	<form action="action_page.php">
			<input list="browsers">
			<datalist id="browsers">
				<option value="Internet Explorer">
				<option value="Firefox">
				<option value="Chrome">
			</datalist>
			<input type="submit">
			</form>
	--	<keygen> element
		to provide a secure way to authenticate users
		specifies a key-pair generator field in a form
		when the form is submitted, two keys are generated, one private and one public
		the private key is stored locally, and the public key is sent to the server
		the public key could be used to generate a client certificate to authenticte the user in the future
		eg.	<form action="action_page.php">
			Username:<br> 
			<input type="text" name="user">
			<br><br>
			Encryption: <br>
			<keygen name="security"> (2048 high grade, or 1024 middle grade)
			<br><br>
			</form>
	--	<output> element
		represents the result of a calculation
		eg. <form action="action_page.php" oninput="x.value=parseInt(a.value) + parseInt(b.value)">
		0
		<input type="range" id="a" name="a" value="50">
		100 +
		<input type="number" id="b" name="b" value="50">
		=
		<output name="x" for="a b"></output>
		<br><br>
		<input type="submit">
		</form>

29.	HTML Input types
	--	text
		<input type="text">
		defines a one-line input field for text input
	--	password
		<input type="password">
		defines a password field (masked as asterisks or circles)
		eg. User name:<br>
			<input type="text" name="userid">
			<br>
			User password:<br>
			<input type="password" name="psw">
	--	submit
		<input type="submit">
		defines a button for submitting form input to a form-handler
	--	radio
		<input type="radio">
		defines a radio button (let a user select ONLY ONE of a limited number of choices)
	--  checkbox
		<input type="checkbox">
		let a user select ZERO or MORE options of a limited number of choices
	--	button
		<input type="button">
		defines a button
	--	number
		<input type="number">
		used for input fields that should contain a numeric value
		you can set restrictions on the numbers
		eg. <form action="">
				Quantity (between 1 and 5):
				<input type="number" name="quantity" min="1" max="5">
			</form>
		other restrictions:
		- disabled
		- max/min (max/min value for an input field)
		- maxlength (max number of character for an input field)
		- pattern (regular expression to check the input value)
		- readonly (cannot be changed input field)
		- required (must be filled out input field)
		- size (width in chars of an input field)
		- step (legal number intervals for an input field)
		- value (default value for an input field)
	--  date 
		<input type="date">
		used for input fields that should contain a date (not support in IE)
	-- 	color
		<input type="color">
		used for input fields that should contain a color (not support in IE)
		eg.	<form>
				Select your favorite color:
				<input type="color" name="favcolor" value="#ff0000">
			</form>
	-- 	range
		<input type="range">
		used for input fields that should contains a value within a range (displayed as a slider control)
		eg.	<form action="action_page.php" method="get">
				Points:
				<input type="range" name="points" min="0" max="10">
			</form>
	--	month
		<input type="month">
		allows the user to select a month AND year (not support in IE)
		eg. <form>
				Birthday (month and year):
				<input type="month" name="bdaymonth">
			</form>
	--	week
		<input type="week">
		allows the user to select a week and year (not support in IE)
		eg.	<form>
				Week:
				<input type="week" name="year_week">
			</form>
	--	time
		<input type="time">
		allows user to select a time (no time zone) (not support in IE)
		eg.	<form>
				Time:
				<input type="time" name="usr_time">
			</form>
	--	datetime
		<input type="datetime">
		allows the user to select a date and time (with time zone) (not support in Chrom, Firefox, IE)
	--  datetime-local
		<input type="datetime-local">
		allows the user to select a date and time (no time zone) (not support in IE)
	--  email
		<input type="email">
		used for input fields that should contain an e-mail address
		the e-mail address can be automatically validated when submitted
	--	search
		<input type="search">
		used for search fields (behaves like a regular text field)
	--  tel
		<input type="tel">
		used for input fields that should contains a telephone number (only support Safari 8)
	--  url
		<input type="url">
		used for input fields that should contain a URL address
		the url field can be automatically validated when submitted

30.	HTML Input Attributes
	--	value
		specifies the initial value for an input field
	--	readonly
		specifies that the input field is read only
		eg.	<input type="text" name="firstname" value="April" readonly>
	--	disabled
		specifies that the input field is disabled (un-usable and un-clickable)
		disabled elements will NOT be submitted
	--	size
		specifies the size in chars for the input field
	--	maxlength
		specifies the max allowed length for the input field
	HTML5 attributes
	--	autocomplete
		specifies whether a form or input field should have autocomplete on or off
		when autocomplete is on, the browser automatically complete values based on values that the user has entered before
		works with <form> and the following <input> types: text, search, url, tel, email, password, datepickers, range and color
		eg.	<form action="action_page.php" autocomplete="on">
				First Name:<input type="text" name="fname"><br>
				Last Name:<input type="text" name="fname"><br>
				<input type="submit">
			</form>
	--	novalidate
		a <form> attribute
		specifies that form data should not be validated when submitted
	--	autofocus 
		a boolean attribute
		specifies that an <input> element should automatically get focus when the page loads
		eg.	<form action="action_page.php">
				First Name:<input type="text" name="fname" autofocus><br>
				Last Name:<input type="text" name="lname"><br>
				<input type="submit">
			</form>
	--	form
		specifies one or more forms an <input> element belongs to
		if some field is outside the form element, it could use "id" to refer to the form
		eg.	<form action="action_page.php" id="form1">
				First Name: <input type="text" name="fname"><br>
				<input type="submit" value="submit">
			</form>
			Last Name: <input type="text" name="lname" form="form1">
	--	formaction
		specifies the URL of a file that will process the input control when the form is submitted
		overrides the action attribute of the <form> element
		used with type="submit" and type="image"
		eg.	<form action="action_page.php">
				...
				<input type="submit" formaction="demo_admin.asp" value="submit as admin">
			</form>
	--	formenctype
		specifies how the form-data should be encoded when submiiting it to the server
		only for forms with method="post"
		overrides the enctype attribute of the <form> element
		used with type="submit" and type="image"
		eg.	<form action="demo_post_enctype.asp" method="post">
				...
				<input type="submit" formenctype="multipart/form-data" value="Submit as Mult/form-data">
			</form>
	--	formmethod
		defines the HTTP method for sending form-data to the action URL
		overrides the method attribute of the <form> element
		can be used with type="submit" and type="image"
		eg.	<form action="action_page.php" method="get">
				...
				<input type="submit" formmethod="post" formaction="demo_post.asp" value="submit use post">
			</form>
	--	formnovalidate
		a boolean attribute
		specifies that the <input> element should not be validated when submitted
		overrides the novalidate attribute of the <form> element
		can be used with type="submit"
	--	formtarget 
		specifies a name or a keyword that indicates where to display the response that is received after submitting the form
		overrides the target attribute of the <form> element
		can be used with type="submit" and type="image"
		eg.	<form action="action_page.php">
				...
				<input type="submit" formtarget="_blank" value="submit to a new tab">
			</form>
	--	height & width
		specify the height and width of an <input> element
		ONLY used with <input type="image">
		always specify the size of images.
	--	list
		refers to a <datalist> element that contains pre-defined options for an <input> element
	--	min and max
		specify the min and max value for an <value> element
		work with following input types: number, range, date, datetime, datetime-local, month, time and week
	--	multiple
		a boolean attribute
		specifies that the user is allowed to enter more than one value in the <input> element
		works with following input types: email and file
		eg.	<form action="action_page.php">
				Select image: <input type="file" name="img" multiple>
				<input type="submit">
			</form>
	--	pattern
		specifies a regular expression that the <input> element's value is checked against
		works with following input types: text, search, url, tel, email, and password
		use the global title attribute to describe the pattern to help the user
		eg. <form>
				Country code: <input type="text" name="country_code" pattern="[A-Za-z]{3}" title="Three letter country code">
			</form>
	--	placeholder 
		specifies a hint that describes the expected value of an input field (a sample value or a short description of the format)
		the hint is displayed in the input field before the user enters a value
		works with following input types: text, search, url, tel, email, and password
		eg.	<form>
				<input type="text" name="fname" placeholder="John"><br>
				<input type="text" name="lname" placeholder="Smith"><br>
			</form>
	--	required
		a boolean attribute
		specifies that an input field must be filled out before submitting the form
		eg.	<form>
				Username: <input type="text" name="username" required>
			</form>
	--	step
		specifies the legal number intervals for an <input> element
		can be used together with the max and min attributes to create a range of legal values
		
Part II: CSS
