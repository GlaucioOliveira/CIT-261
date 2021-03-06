## Code Topic Fluency 

### AJAX
> Requesting a JSON file.

AJAX stands for **A**synchronous **J**avaScript **A**nd **X**ML. It's a technology that makes use of the XMLHttpRequest object to get/post HTTP responses inside a HTML page.

To make use of the XMLHttpRequest object, we need to create an instance of it, them define a callback function to the event listener **onreadystatechange** of this object. The block of code that we define at this event listener will be executed when something change after we try to make a connection (wih the **open** method).

In the example below we are making a call to an URL with the 'GET' verbose and making it an asynchronous call (the third parameter on the **open** method defines it asynchronous). The returning content of this call is in JSON format.

````html
<script>
function testingAJAX() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    //status 200 => OK (everything is OK)
    if (this.status == 200 && this.readyState == 4){
      document.write("Result from the HTTP Request: <br><br>");
      document.write(this.responseText);
    } 
  };
  
  xhttp.open("GET", "https://api.bitcointrade.com.br/v2/public/BRLBTC/ticker", true);
  xhttp.send();
}
  
  testingAJAX();
</script>
````
<a href="https://codepen.io/glaucioso/pen/wOPmGX" target="_blank">Live Demo (at CodePen)</a>

**NOTE:** the '200 OK status' for HTTP response if defined at the HTTP/1.1 protocol. ([Source](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html))
