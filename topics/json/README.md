## Code Topic Fluency 

### JSON
> Parse, Stringify

JSON stands for **J**ava**S**cript **O**bject **N**otation. According to it's creators definition, it is a lightweight data-interchange format. It's the best choice now a days to exchange data between different applications. 

Example of a JSON file with an Object having two properties (`name` and `surname`):
````json
{
  "name": "Gláucio", 
  "surname": "Oliveira"
}
````

#### Parse
With the `JSON.parse` function, it's possible convert JSON strings into JavaScript Objects. At the example below, the variable `jsonString` is passed as an argument. The result of this method is an Object with the properties `name`, `profession` and `age`.

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
With the `JSON.stringify` function, it's possible to cast JavaScript Objects into a JSON String. Basically it's the inverse process of the Parse function described above. We pass an object as an argument to this function, and the return of this function is a string in the JSON format.

```html
<script>  
  var userObject = {name: 'Gláucio', profession: 'Developer', age: 28};
  var jsonString = JSON.stringify(userObject);
  document.write(jsonString);
</script>
```
<a href="https://codepen.io/glaucioso/pen/eXGBoY" target="_blank">Live Demo (at CodePen)</a>
