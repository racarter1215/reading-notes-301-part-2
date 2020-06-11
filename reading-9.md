# Functional Programming

### It is a programming paradigm - a style of building the structure and elements of computer programs - that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

##### Pure functions: It returns the same result if given the same arguments (it is also referred as deterministic) and it does not cause any observable side effects

##### If a function takes in global or reading files, rng, or makes side effects, it is NOT pure

##### Pure wants functions to be isolated and unable to impact other parts of the system

##### Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result

##### it needs immutability

##### When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

### Referential Transparency

##### pure functions + immutable data = referential transparency

##### if a function consistently yields the same result for the same input, it is referentially transparent

##### Functions as first class entities

##### The idea of functions as first-class entities is that functions are also treated as values and used as data.

##### Functions as first-class entities can refer to it from constants and variables, pass it as a parameter to other functions, and return it as result from other functions

##### Higher-order functions

##### Type of function that either takes one or more functions as arguments or returns a function as its result

##### Filter function: expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection

# Refactoring JavaScript for Performance and Readability

### Scenario 1

##### // Unrefactored code

##### const URLstore = [];

##### function makeShort(URL) {
#####   const rndName = Math.random().toString(36).substring(2);
#####   URLstore.push({[rndName]: URL});
#####   return rndName;
##### }

##### function getLong(shortURL) {
#####   for (let i = 0; i < URLstore.length; i++) {
#####     if (URLstore[i].hasOwnProperty(shortURL) !== false) {
#####       return URLstore[i][shortURL];
#####     }
#####   }
##### }

##### Problem: what happens if getLong is called with a short URL that isn't in the store? Nothing is explicitly returned so undefined will be returned. Since we're not sure how we're going to handle that, let's be explicit and throw an error so that problems can be spotted during development.

##### Performance-wise, be careful if you're iterating through a flat array very often, especially if it's a core piece of your program. The refactor here is to change the data-structure of URLstore.

##### Currently, each URL object is stored in an array. We'll visualize this as a row of buckets. When we want to convert short to long, on average we need to check half of those buckets before we find the correct short URL. What if we have thousands of buckets, and we perform this hundreds of times a second?

##### The answer is to use some form of hash function, which Maps and Sets use under the surface. A hash function is used to map a given key to a location in the hash table.

##### Example

##### // Refactored code

##### const URLstore = new Map(); // Change this to a Map

##### function makeShort(URL) {
#####   const rndName = Math.random().toString(36).substring(2);
#####   // Place the short URL into the Map as the key with the long URL as the value
#####   URLstore.set(rndName, URL);
#####   return rndName;
##### }

##### function getLong(shortURL) {
#####   // Leave the function early to avoid an unnecessary else statement
#####   if (URLstore.has(shortURL) === false) {
#####     throw 'Not in URLstore!';
#####   }
#####   return URLstore.get(shortURL); // Get the long URL out of the Map
##### }
