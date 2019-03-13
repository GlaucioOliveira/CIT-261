## Code Topic Fluency 

### AJAX
> Requesting a JSON file.

AJAX stands for **A**synchronous **J**avaScript **A**nd **X**ML. It's a technology that makes use of the XMLHttpRequest object to get/post HTTP responses.

To make use of the XMLHttpRequest object, we need to create an instance of it, then define a callback function to the event listener **onreadystatechange** of this object. The block of code that we define at this event listener will be executed when something change after we try to make a connection (wih the **open** method).

In the example below we are making a call to a URL with the 'GET' verbose and making it an asynchronous call with the value 'true' especified on the third position of the **open** method.

```html
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
```
<a href="https://codepen.io/glaucioso/pen/wOPmGX" target="_blank">Live Demo (at CodePen)</a>
