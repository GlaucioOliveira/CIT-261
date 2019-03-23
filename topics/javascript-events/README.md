## Code Topic Fluency 

### JavaScript Events
> Standard JavaScript Events Including those for Mobile Devices and Animation and Transition Events.

With JavaScript Events we are able to know or to react when the user is interacting with any HTML Element.

Calling to events can be inline:

````html
<button onclick="alert('Hello World!')">Inline Event Call</button>
```` 

On the Example above, when the user click the button, it will be displayed the message 'Hello World'. We can also call an inline function that it's defined on a `<script>` tag:

````html
<script>
  function displayMessage(){
    alert('Hello World!');
  }
</script>
<button onclick="displayMessage()">Inline Event Call to a function</button>
````

Another possibility to respond to an event is with the DOM. We can create an Event Listener (`addEventListener`) to the HTML Element and specify the event type (in the example the `'click'`):

````html
<script>
  function displayMessage(){
    alert('Hello World!');
  }
  
  document.getElementById('button1').addEventListener('click', displayMessage);
  
</script>
<button id="button1" onclick="displayMessage()">Inline Event Call to a function</button>
````
<a href="https://codepen.io/glaucioso/pen/EMrgrb" target="_blank">Live Demo (At CodePen)</a>

*NOTE:* A list with [all possible event types for any HTML Element](https://developer.mozilla.org/en-US/docs/Web/Events)
