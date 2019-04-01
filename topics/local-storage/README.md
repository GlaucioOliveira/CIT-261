## Code Topic Fluency 

### Local Storage
> API, Storing and Retrieving Simple Data, Arrays, Associative Arrays, and Objects.

With the `localStorage` object from JavaScript, we are able to create information and store it on the Client Browser. In the past this was only possible with Cookies which had a very limited size (4093 bytes per domain).

Local Storage is more efficient and allows more information to be stored. The limitation of size depends on the browser used (<a href="https://developer.chrome.com/apps/offline_storage" target="_blank">For Chrome the default limit it's 5 MBs</a>). Below there is an example of working with Local Storage to store Simple data, arrays, and objects.

**NOTE**: To save Objects on Local Storage, we need to [cast the JavaScript object into a JSON string](../json/README.md#Stringify) (with the JSON.stringify function) and them save the result (the string). To restore the information as an object, we need to use the [JSON parse function to turn the string back into an Object](../json/README.md#Parse).

Above there are examples of how to save strings, arrays and objects with local Storage:

````html
<script>  
  function saveUserName(){
    localStorage.setItem("userName","glaucio.oliveira");
  }
  
  function loadUserName(){
    document.getElementById("txtUserName").value = localStorage.getItem("userName");
  }
  
  function saveArray(){
    var array = ['Apple','Banana','Cherry'];
    localStorage.setItem("array",array);
  }
  
  function loadArray(){
    document.getElementById("txtArray").value = localStorage.getItem("array");
  }
  
  function saveObject(){
    var object = {name: "Gláucio", age: 28};
    localStorage.setItem("object", JSON.stringify(object));    
  }
  
  function loadObject(){
    var JSONObject = localStorage.getItem("object");
    if(JSONObject != undefined){
      var realObject = JSON.parse(JSONObject);
      document.getElementById("txtObject").value = "name: " + realObject.name + ", age: " + realObject.age + ".";
    }
  }  
</script>
````

Rich apps can be created with localStorage. In the link below there is a TODO App that store a list of TODO itens on local Storage.
<a href="https://codepen.io/glaucioso/pen/MxrLGV" target="_blank">Live Demo of TODO App (At CodePen)</a>
