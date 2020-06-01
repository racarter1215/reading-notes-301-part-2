# EJS

### Evaluate an injected variable, iterate/loop over an array of values, if/else statements, layouts, and partials

##### do an npm init -y

##### npm install  --save express body-parser cors ejs

##### var express = require('express');
##### var bodyParser = require('body-parser');
##### var cors - require('cors');
##### path = require('path');
##### var app = express();

##### app.use(bodyParser());
##### app.use(cors());

##### app.set('views', path.join(__dirname, 'views'));

##### app.set('view engine', 'ejs');

##### create a new folder called views/index.ejs

##### put generic text in there (like hello world)

##### app.listen(8000, function() {
#####     console.log('heard on 8000')
##### });

##### app.get('/', function(request, response) {
#####     response.render('index', {
#####     foo: 'bar'
##### });
##### })

### Evaluate injected variable

##### within index.ejs file, replace hello world with foo (and have a %= before it)
