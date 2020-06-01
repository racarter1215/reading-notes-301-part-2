# Javascript Templating Language and Engine

### Javascript Templating: a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source.

##### The template is HTML markup, with added templating tags that will either insert variables or run programming logic.

### Mustache: a logic-less template syntax. It can be used for HTML, config files, source code, or anything else you can imagine.

##### Logic-less: there are no if statements, else clauses, or for loops. Instead, there are only tags. Some tags are replaced with a value, some nothing, and others a series of values.

##### mustache.js is an implementation of the mustache template system in JavaScript. It is often considered the base for JavaScript templating. 

##### Mustache.render(“Hello, {{name}}”, { name: “Sherlynn” });
##### // returns: Hello, Sherlynn

##### {{ name }} = mustache syntax for a placeholder

##### Mustache is NOT a templating engine. Mustache is a specification for a templating language.

##### If you intend you use mustache with Node and Express, you can use mustache-express.

##### When using yarn: $ yarn add mustache-express

##### When using node: $ npm install mustache --save

# A Guide to Flexbox

### Flexbox Layout aims at providing a more efficient way to lay out, align and distribute space among items in a container, even when their size is unknown and/or dynamic

##### It give the container the ability to alter its items’ width/height (and order) to best fill the available space (mostly to accommodate to all kind of display devices and screen sizes).

##### the flexbox layout is direction-agnostic as opposed to the regular layouts (block which is vertically-based and inline which is horizontally-based).

###### Flexbox layout is most appropriate to the components of an application, and small-scale layouts, while the Grid layout is intended for larger scale layouts.

##### Items will be laid out following either the main axis (from main-start to main-end) or the cross axis (from cross-start to cross-end).

### Word Bank

###### main axis – The main axis of a flex container is the primary axis along which flex items are laid out. Beware, it is not necessarily horizontal; it depends on the flex-direction property (see below).
###### main-start | main-end – The flex items are placed within the container starting from main-start and going to main-end.
###### main size – A flex item’s width or height, whichever is in the main dimension, is the item’s main size. The flex item’s main size property is either the ‘width’ or ‘height’ property, whichever is in the main dimension.
###### cross axis – The axis perpendicular to the main axis is called the cross axis. Its direction depends on the main axis direction.
###### cross-start | cross-end – Flex lines are filled with items and placed into the container starting on the cross-start side of the flex container and going toward the cross-end side.
###### cross size – The width or height of a flex item, whichever is in the cross dimension, is the item’s cross size. The cross size property is whichever of ‘width’ or ‘height’ that is in the cross dimension.

##### display
###### This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.

###### .container {
######   display: flex; /* or inline-flex */
###### }

##### flex direction
###### .container {
######   flex-direction: row | row-reverse | column | column-reverse;
###### }

##### .container{
#####   flex-wrap: nowrap | wrap | wrap-reverse;
##### }
