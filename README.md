<?php
//echo"Creation of scam data base<br>";
//echo"..................<br>";
$servername="localhost";
$username="root";
$password="";
$dbname="scam";
$tbl_name="personal";
$conn=mysqli_connect($servername,$username,$password,$dbname);
if(!$conn)
{
die("connection failed: ".mysqli_connect_error());
}
else
{
//echo".............";
$name=$_POST["name"];
$age=$_POST["age"];
$email=$_POST["email"];
$no=$_POST["no"];
$addre=$_POST["addre"];
$sql="insert into personal(name,age,email,no,addre)VALUES('$name','$age','$email','$no','$addre')";
if(mysqli_query($conn,$sql))
{
	echo"<center><b> Your details added successfully<b></center>";
	echo"<BR>";
}
}
?>
<html>
<head><title>Tour and travel</title>
<style>
body{
background-image:url("world.jpg");
background-repeat:no repeat;
}
</style>
</head>
<body>
</br></br></br>
<big><big><center><a href="booktrip.php">Booktrip</a></center></big></big>
</body>
</html>
