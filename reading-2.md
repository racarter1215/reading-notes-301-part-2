# jQuery

### What is it?

##### It's a JavaScript file that you include in your web pages.
##### It lets you find elements using CSS-style selectors and then do something with the elements using jQuery methods.

##### Find elements using css-style selectors
###### jQuery() lets you find one or more elements in the page. It creates an object called jQuery which holds references to those elements. $() is often used as a shortand for jQuery(). 
##### It's kinda like a DOM query, but much simpler syntax

##### jQuery object has many methods that you can use to work with the elements you select. The methods represent tasks that you commonly need to perform with elements.

##### Example: $('li.hot').addClass('complete'); This line of code starts with a matched set (li.hot), follwed by a member operator "." and a method (addClass('complete')); Each method attached to a jQuery has a parameter(s) that provide details about how to update the elements.

### Matched set/ jQuery selection

##### When you select one or more elements, a jQuery object is returned. It is also known as a matched set or a jQuery selection.

##### Single element: If a selector returns one element, the jQuery object contains a reference to just one element node. Example: $('ul')

##### Multiple elements: If a selector returns several elements, the jQUery object contains references to each element. Example: $('li')

##### JQuery methods that get and set data

##### Get information: If a jQuery selection holds more than one element, and a method is used to get info from the selected elements, it will retrieve info from only the first element in a matched set. When you use the .html() method to get info from an element, it will return the content of the first element in the matched set.

##### Set information: If a jQuery selection holds more than one element, and a method is used to update information on the page, it will update all of the elements in the matched set, not just the first one. When you use the .html() method to update the element, it will replace the contents of each element in the matched set.

##### When you create a jQuery selection, the jQuery object holds references to the elements in the DOM, it does not create a copy of them.

##### A jQuery object stores references to elements. Caching a jQuery object stores a reference to it in a variable.

### Looping

##### With jQuery, when a selector returns multiple elements, you can update all of them using the one method. There is no need to use a loop. 

### Chaining

##### If you want to use more than one jQuery method on the same selection of elements, you can list several methods at a time using dot notation to separate each one, as shown below.

##### METHODS TO RETRIEVE INFROMATION FROM THE DOM CANNOT BE CHAINED

##### jQuery's .ready() method checks that the page is ready for your code to work with.

##### Example: $(document).ready(function() { // your script goes here });

##### .load() is replaced by .on()

##### A shortcut for ready event method on document object: $(function() {// your script goes here});

### Getting element content

##### .html() is used to retrieve info from a jQuery selection, it retrieves only the HTML inside the FIRST element in the matched set, along with any descendants. 

##### .text() is used to retreive the text from a jQuery selection, it returns the content from every element in the jQuery selection, along with the text from any descendants. 

##### Updating Elements

##### 4 methods that update the content of all elements in a jQuery selection: .html(), .text(), .replaceWith(), and .remove().

### Changing content

### Inserting ELements

##### Involves two steps, create the new elements in a jQuery object and use a method to insert the content into the page.

##### adding new elements can be accomplished by: .before(), .after(), .prepend(), and .append()

### Getting and Setting CSS properties

##### the .css() method lets you retrieve and set the values of CSS properties.

##### To GET the value of a CSS property, you indicate which property you want to retrieve in parentheses. If the matched set contains more than one element, it will return the value from the first element. var backgroundColor = $('li').css('background-color');

##### To SET the values of a CSS property, you specify the property name as the first argument in the parentheses, then a comma, followed by its value as the second argument. This will update every element in the matched set. You can also specify multiple properties in the same method using object literal notation. $('li').css('background-color', '#272727');

##### To set a value in pixels, do: $('li').css('padding-left', '+=20');

##### Working with each element in a selection: .each() allows you to perform one or more statements on each of the items in the selection of elements that is returned by a selector, like a loop. this or $(this) uses the this keyword to create a new jQuery selection containing the current element. It allows you to use jQuery methods on the current element.

### Event Methods

##### The .on() method is used to handle all events. Behind the scenes, jQuery handles all of the cross-browser issues you saw in the last chapter. Page 326 has list of on events

# 6 Reasons for Pair Programming

### While learning to code, developers likely study several programming languages. Similar to a foreign language class, there are four fundamental skills that help anyone learn a new language: Listening: hearing and interpreting the vocabulary Speaking: using the correct words to communicate an idea Reading: understanding what written language intends to convey Writing: producing from scratch a meaningful

##### Pair programming touches on all four skills: developers explain out loud what the code should do, listen to others’ guidance, read code that others have written, and write code themselves.

##### Greater efficiency
##### Engaged collaboration
##### Learning from fellow students
##### Social skills
##### Job interview readiness
##### Work environment readiness
