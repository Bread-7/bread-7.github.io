# Header
oogabooga

## Heading level 2

Here is some text with an <span style="color:blue">inline blue text</span>.
<div>
  <p>This is a paragraph inside a div container.</p>
  
</div>
<script type="text/javascript" src="scripts.js"></script>
<script>
  function setStorage(){
    const json = { "example": "data" }; // replace with your own JSON data
    const jsonStr = JSON.stringify(json);
    const blob = new Blob([jsonStr], { type: "application/json" });
    const url = URL.createObjectURL(blob);

    const downloadLink = document.createElement("a");
    downloadLink.setAttribute("href", url);
    downloadLink.setAttribute("download", "example.json"); // replace with your desired filename
    document.body.appendChild(downloadLink);
    downloadLink.click();
    document.body.removeChild(downloadLink);

    URL.revokeObjectURL(url); // clean up the blob URL when done
  }
</script>
<!-- <script type = "module">
  import cube from '/scripts.js'
  console.log(cube(3))
  
</script> -->

<button type="button" onclick="document.getElementById('demo').innerHTML = Date()">
Click me to display Date and Time.</button>

<p id="demo"></p>

<label for="fname">First name:</label>
<input type="text" id="fname" name="fname"><br><br>
<input type="text" id="lname" name="lname"><br><br>
<input type="button" id="submit" value="Submit" onclick="setStorage()" />



<!-- <button onclick="runPython()">Run Python</button>
  <script>
    function runPython() {
      // Make an AJAX request to a Python script
      var xhr = new XMLHttpRequest();
      xhr.open("GET", "index.py", true);
      xhr.send();
    }
  </script> -->