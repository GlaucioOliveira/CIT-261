## Code Topic Fluency 

### Local Storage
> API, Storing and Retrieving Simple Data, Arrays, Associative Arrays, and Objects.

With the **LocalStorage** object from JavaScript, we are able to create information and store it on the client browser. In the past this was only possible with Cookies which had a very limited size (4093 bytes per domain).

Local Storage is much more efficient and allows more information to be stored (the limitation depends on the browser). <a href="https://developer.chrome.com/apps/offline_storage" target="_blank">For Chrome it's 5 MBs the default limit</a>. Below there is an example of working with Local Storage to store Simple data, arrays, and objects.

**NOTE**: To save Objects on LocalStorage, we need to cast the object into a JSON string (with the JSON.stringify function) and them save the result (the string). To restore the information we need to use the JSON parse to turn the string back into an Object. This is also demonstrated on the code below.

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
  
  function cleanUp(){
    localStorage.removeItem("userName");
    localStorage.removeItem("array");
    localStorage.removeItem("object");
    
    document.getElementById("txtUserName").value = "";
    document.getElementById("txtArray").value = "";
    document.getElementById("txtObject").value = "";
    
    alert('All cleaned up!');
  }  
</script>

<div>
  <button onclick="cleanUp()">Clear All Data</button>
</div>
  <h3>Storing Simple Data</h3>
  <input type="text" id="txtUserName" disabled placeholder="User Name" />
  <button onclick="saveUserName()">Save Text</button>
  <button onclick="loadUserName()">Load Text</button>
</div>

<div>
  <h3>Storing Arrays</h3>
  <input type="text" id="txtArray" disabled placeholder="Array List" />
  <button onclick="saveArray()">Save Array</button>
  <button onclick="loadArray()">Load Array</button>
</div>

<div>
  <h3>Storing Object</h3>
  <input type="text" id="txtObject" disabled placeholder="Object Content" />
  <button onclick="saveObject()">Save Object</button>
  <button onclick="loadObject()">Load Object</button>
</div>
````
<a href="https://codepen.io/glaucioso/pen/MxrLGV" target="_blank">Live Demo (CodePen)</a>
