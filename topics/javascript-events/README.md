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

With the DOM we can also create an Event Listener to the HTML Element:

````html
<script>
  function displayMessage(){
    alert('Hello World!');
  }
  
  document.getElementById('button1').addEventLister('click', displayMessage);
  
</script>
<button id="button1" onclick="displayMessage()">Inline Event Call to a function</button>
````

<a href="https://codepen.io/glaucioso/pen/EMrgrb" target="_blank">Live Demo (At CodePen)</a>
