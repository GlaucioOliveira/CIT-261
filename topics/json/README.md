## Code Topic Fluency 

### JSON
> Parse, Stringify

JSON stands for **J**ava**S**cript **O**bject **N**otation.

#### Parse
With this function from the JSON object we are able to convert JSON strings into JavaScript Objects. At the example below, the variable jsonString is passed as an argument for the JSON.parse method. The result of this method is an Object.

```html
<script>
  var jsonString = '{ "name":"Gláucio", "profission":"Developer", "age":28}';
  var jsonObject = JSON.parse(jsonString);
  document.write("Hi, my name is " + jsonObject.name + ". <br/>");
  document.write("I'm with " + jsonObject.age + " old, and I'm a " + jsonObject.profission + "."); 
</script>
```
<a href="https://codepen.io/glaucioso/pen/eXGBPq" target="_blank">Live Demo (at CodePen)</a>


#### Stringify
With Stringify we are able to cast JavaScript Objects to Json string. So basically it's the inverse process of the Parse function. We pass an object as a argument, and the return is a string.

```html
<script>  
  var userObject = {name: 'Gláucio', profession: 'Developer', age: 28};
  var jsonString = JSON.stringify(userObject);
  document.write(jsonString);
</script>
```
<a href="https://codepen.io/glaucioso/pen/eXGBoY" target="_blank">Live Demo (at CodePen)</a>
