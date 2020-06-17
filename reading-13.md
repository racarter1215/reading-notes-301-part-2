# Sending form data

###  the web uses a client/server architecture that can be summarized as follows. a client, like a web browser, sends a request to a server like Apache or Nginx, using the HTTP protocol. The server answers the request using the same protocol.

##### HTML forms on a web page are nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.

##### The <form> element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are action and method.

##### Action Attribute: this defines where the data gets sent. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.

##### When specified with no attributes, the <form> data is sent to the same page that the form is present on

##### The names and values of the non-file form controls are sent to the server as name=value pairs joined with ampersands. The action value should be a file on the server that can handle the incoming data, including ensuring server-side validation. The server then responds, generally handling the data and loading the URL defined by the action attribute, causing a new page load.

##### Method Attribute: defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the GET method and the POST method

##### GET Method: the method used by the browser to ask the server to send back a given resource.

##### POST Method: the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request.

##### HTTP requests are never displayed to the use

##### The only thing displayed to the user is the URL called. As we mentioned above, with a GET request the user will see the data in their URL bar, but with a POST request they won't. 

##### If you need to send a password, never use the GET method or you risk displaying it in the URL bar, which would be very insecure. Instead, the POST method is preferred because some browsers limit the sizes of URLs. In addition, many servers limit the length of URLs they accept.

##### PHP offers some global objects to access the data. 

##### <?php
  // The global $_POST variable allows you to access the data sent with the POST method by name
  // To access the data sent with the GET method, you can use $_GET
  $say = htmlspecialchars($_POST['say']);
  $to  = htmlspecialchars($_POST['to']);

  echo  $say, ' ', $to;
?>

