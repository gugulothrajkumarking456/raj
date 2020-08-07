<html>
<head> 
	<meta charset="utf-8"> 
	<meta name="viewport"
		content="width=device-width, initial-scale=1"> 
        <body style="background-color:powderblue;">
	<style>
    style="background-color:powderblue;">
		div { 
			width: 300px; 
			height: 100px;
			padding: 15px; 
			position: static; 
			left:30%; 
		} 
	</style> 
    </body>
</head> 

<form action="action_page.php">
  
 <center> <h1 style="color:red">Student Registration Form</h1> </center>
     
 <!--HTML CODE FOR ENTERING NAME & LAST NAME IN THE TEXT BOX ONLY CHARECTER  -->   

  <center>  <label for="Name">
  
       <b>Name:</b> 
  <br>
  <br>
  </label>
    <div class="container"> 
    <input type="text" placeholder="Enter Name" name="Name" id="txt" size="20" onkeyup="manage(this)" onkeypress="return (event.charCode > 64 && event.charCode < 91) || (event.charCode > 96 && event.charCode < 123)" required>

 
<br>
<br>



 <label for="Lastname"><b>Lastname:</b></label>
 <br>
 <br>
 <div class="container"> 
 <input type="text" placeholder="Enter Lastname" name="Name" id="txt" size="20" onkeyup="manage(this)" onkeypress="return (event.charCode > 64 && event.charCode < 91) || (event.charCode > 96 && event.charCode < 123)"
required>
<br>
<br>
<!--HTML CODE FOR ENTERING CLASS WITHOUT SPECIAL CHARECTER -->   

<label for="Class"><b>Class:</b></label>
<br>
<br>
    <div class="container">   
      <input type="text"placeholder="Enter Class" name="Name" id="txt"onkeyup="manage(this)" onkeypress="return blockSpecialChar(event)"/>
      <br>
      <br>
    <label for="Year of passing"><b>Year of passing:</b></label>
    <br>
    <br>
    <div class="container"> 
<input type="date" id="myDate" name="bday" min="1990-01-01" max="2017-12-31">
<p id="demo"></p>
 
	<div class="container"> 
		<form name="inputnumber" 
			autocomplete="off"> 
			<b>Percentage:</b> 
            <br>
            <br>
			<input type="text" placeholder="Enter Percentage"
				onkeypress="return onlyNumberKey(event)"
				
				 /> 

			<br> 
			<br>
			<br> 
			
				
			
		</form> 
        
	
<bottom>
<input type="submit" id="btSubmit" disabled / onclick="myFunction()"> </bottom>
    


 <!--SCRIPT FOR ENTERING NAME & LAST NAME IN THE TEXT BOX ONLY CHARECTER  --> 
<script type="text/javascript">
    function blockSpecialChar(e){
        var k;
        document.all ? k = e.keyCode : k = e.which;
        return ((k > 64 && k < 91) || (k > 96 && k < 123) || k == 8 || k == 32 || (k >= 48 && k <= 57));
        }
    </script>
        <!--SCRIPT FOR ENTERING DATE SHOULD BE BEFORE 2017  --> 

    <script>
function myFunction() {
  var x = document.getElementById("myDate").max = "2016-12-31";
  document.getElementById("demo").innerHTML = "Enter only before 2017";
}
</script>  
<!--SCRIPT FOR ENTERING ONLY NUMBERS IN THE PERCENTAGE TEXTBOX-->

<script> 
	function onlyNumberKey(evt) { 
		
		// Only ASCII charactar in that range allowed 
		var ASCIICode = (evt.which) ? evt.which : evt.keyCode 
		if (ASCIICode > 31 && (ASCIICode < 48 || ASCIICode > 57)) 
			return false; 
		return true; 
	} 
</script> 


<!--SCRIPT FOR DISABLE THE SUBMIT BUTTON BEFORE ENTERING THE DATA AND ENABLEING THE BUTTON AFTER ENTERING THE DATA-->

<script>


	function manage(txt) {
        var bt = document.getElementById('btSubmit');
        if (txt.value != '') {
            bt.disabled = false;
        }
        else {
            bt.disabled = true;
        }

}
    </script>
  </div>
</form>
</html>
