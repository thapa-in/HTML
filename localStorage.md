
Create Html file and add this code and run

```
<div id="result"></div>
<script>

// Check browser support
if (typeof(Storage) !== "undefined") {
	 var debtors = '{"ledger":[{"ln":"A", "grp":"D", "adr":"55", "state":"up", "city":"lko", "pin":"", "mob":"", "email":"email@gmail.com", "gstn":"-","ac":"","ifsc":"","bank":"","bnkadr":""}, {"ln":"B", "grp":"D", "adr":"55", "state":"up", "city":"lko", "pin":"", "mob":"", "email":"email@gmail.com", "gstn":"-","ac":"","ifsc":"","bank":"","bnkadr":""}]}'
  // Store
  localStorage.setItem("debtors", debtors);
  var jsondata = JSON.parse(localStorage.getItem("debtors"));
  
  document.getElementById("result").innerHTML = jsondata.ledger[1].ln;
  // Retrieve
  //document.getElementById("result").innerHTML = localStorage.getItem("debtors");
} else {
  document.getElementById("result").innerHTML = "Sorry, your browser does not support Web Storage...";
}
</script>
```
