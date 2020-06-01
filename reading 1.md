# Responsive Web Design

### Mobile Internet usage is growing rapidly and now we need to build websites suitable for all users. The industry response to this question has become responsive web design.

##### Responsive web design: the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.

### Responsive vs. Adaptive vs. Mobile

##### Responsive: generally means to react quickly and positively to any change.

##### Adaptive: means to be easily modified for a new purpose or situation, such as change.

##### Responsive design websites continually and fluidly change based on different factors, such as viewport width, while adaptive websites are built to a group of preset factors.

##### Mobile: generally means to build a separate website commonly on a new domain solely for mobile users. 

##### Responsive web design is the most popular now, favoring design that dynamically adapts to different browser and device viewports, changing layout and content along the way. 

### Flexible Layouts

##### Responsive web design is broken down into three main components: flexible layouts, media queries, and flexible media.

##### Flexible Layouts: the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width.

###### Flexible grids are built using relative length units, most commonly PERCENTAGES or EM units. These relative lengths are then used to declare common grid property values such as width, margin, or padding.

##### Flexible layouts don't like to use fixed measurement units because the viewport height and width continually change from device to device.

##### target ÷ context = result!!!!!!

### Flexible Grid

##### HTML
##### <div class="container">
#####   <section>...</section>
#####  <aside>...</aside>
##### </div>

##### CSS
##### .container {
#####   width: 538px;
##### }
##### section, 
##### aside {
#####  margin: 10px;
##### }
##### section {
#####   float: left;
#####   width: 340px;
##### }
##### aside {
#####   float: right;
#####   width: 158px;
##### }

##### Now, with Flexible Grid:

##### section,
##### aside {
#####   margin: 1.858736059%; /*  10px ÷ 538px = .018587361 */
##### }
##### section {
#####   float: left;
#####   width: 63.197026%;    /* 340px ÷ 538px = .63197026 */   
##### }
##### aside {
#####   float: right;
#####   width: 29.3680297%;  /* 158px ÷ 538px = .293680297 */

##### One can also leverage the min-width, max-width, min-height, and max-height properties for greater control of the webpage.

### Media Queries

##### Media Queries: Provide the ability to specify different styles for individual browser and device circumstances, such as the width of the viewport or device orientation.

##### Multiple ways to use media queries, including using the @media rule inside of an existing style sheet, importing a new style sheet using the @import rule, or by linking to a separate style sheet from within the HTML document.

###### @media is recommended inside of an existing style sheet to avoid unwanted HTTP requests.

##### HTML
##### <!-- Separate CSS File -->
##### <link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)">

##### CSS
##### /* @media Rule */
##### @media all and (max-width: 1024px) {...}

##### /* @import Rule */
##### @import url(styles.css) all and (max-width: 1024px) {...}

##### Each media query may include a media type followed by one or more expressions. Common media types include all, screen, print, tv, and braille. 

##### The HTML5 specification includes new media types, even including 3d-glasses. 

##### Should a media type not be specified the media query will default the media type to screen.

##### The media query expression that follows the media type may include different media features and values, which then allocate to be true or false.

### Logical Operators in Media Queries

##### The three logical operators used within media queries are and, not, and only.

##### Using the "and" logical operator within a media query allows an extra condition to be added.

###### Example: @media all and (min-width: 800px) and (max-width: 1024px) {...}

##### The "only" logical operator is a new operator and is not recognized by user agents using the HTML4 algorithm, thus hiding the styles from devices or browsers that don’t support media queries.

###### Example: @media only screen and (orientation: portrait) {...}

### Media Features in Media Queries

##### Media features identify what attributes or properties will be targeted within the media query expression.

##### A common media features is determining a height or width for a device or browser viewport. 

###### Example: @media all and (min-width: 320px) and (max-width: 780px) {...}

##### Using min and max prefixes avoid any conflict with the general HTML syntax, specifically not using the < and > symbols.

##### orientation media feature determines if a device is in the landscape or portrait orientation.

##### The landscape mode is triggered when the display is wider than taller, and the portrait mode is triggered the opposite way.

###### Example: @media all and (orientation: landscape) {...}

##### The aspect-ratio and device-aspect-ratio features specifies the width/height pixel ratio of the targeted rendering area or output device. The min and max prefixes are available to use with the different aspect ratio features, identifying a ratio above or below that of which is stated.

###### Example: @media all and (min-device-aspect-ratio: 16/9) {...}

##### Pixel-ratio: great for identifying high definition devices, including retina displays.

###### Example: @media only screen and (-webkit-min-device-pixel-ratio: 1.3), only screen and (min-device-pixel-ratio: 1.3) {...}

### Mobile First

##### Mobile First includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.

###### Example: /* Default styles first then media queries */
###### @media screen and (min-width: 400px)  {...}
###### @media screen and (min-width: 600px)  {...}
###### @media screen and (min-width: 1000px) {...}
###### @media screen and (min-width: 1400px) {...}

### Viewport

##### Using the viewport meta tag with either the height or width values will define the height or width of the viewport respectively.

###### Each value accepts either a positive integer or keyword. For the height property the keyword device-height value is accepted, and for the width property the keyword device-width is accepted.

### Flexible Media

##### Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

###### Example: img, video, canvas {
######   max-width: 100%;
###### }

# All About Floats

### What is a Float?

##### It is a CSS positioning property.

##### By using Float, one can ignore the text wrap and allow words to flow right over the image like it wasn’t even there.

##### Floated elements remain a part of the flow of the web page.

###### Example: sidebar {
######   float: right;			
###### }



 




