# Heroku

### The Heroku CLI requires Git.

### Download it by using: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

##### heroku login gets you on:

##### heroku login
##### heroku: Press any key to open up the browser to login or q to exit
#####  ›   Warning: If browser does not open, visit
#####  ›   https://cli-auth.heroku.com/auth/browser/***
##### heroku: Waiting for login...
##### Logging in... done
##### Logged in as me@example.com

##### Click Log In when it is displayed
###### This authentication is required for both the heroku and git commands to work correctly

##### To clone a local version of the sample application that you can then deploy to Heroku, execute the following commands in your local command shell or terminal:|
###### git clone https://github.com/heroku/node-js-getting-started.git
###### cd node-js-getting-started

##### to deploy the app, you need to run the following code:
###### heroku create
###### Creating sharp-rain-871... done, stack is heroku-18
###### http://sharp-rain-871.herokuapp.com/ | https://git.heroku.com/sharp-rain-871.git
###### Git remote heroku added

##### you deploy the code through git push heroku master

##### you open the app by heroku open

##### you can view heroku logs by typing heroku logs --tail

##### CTRL + C stops the logs from showing
