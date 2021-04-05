<DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Normal log in form</title>
<style type="text/css">
form{
width: 600px;
margin: 200px auto;
}
div{
width: 100%;
margin: 15px auto;
}
label{
display: block;
padding: 20px;
font-size: 25px;
}

input{
width: 96%;
padding: 10px;
border: 1px solid #797979;
font-size: 20px;
margin-left: 20px;
border-radius: 3px;
}
button{
margin: 20px;
padding: 10px;
width: 100px;
border: none;
outline: none;
cursor: pointer;
border-radius: 5px;
font-size: 20px;
font-weight: bold;
color: whitesmoke;
background: linear-gradient(90deg, royalblue, lightgreen);
}
span{
display:block;
margin-left: 20px;
color: red;
font-style: italic;
</style>
</head>
<body>

<form action="swipe.html" method="POST">
<div>
<label for="username">Username</label>
<input type="text" name="username" placeholder="username">
<span></span>
</div>
<div>
<label for="password">Password</label>
<input type="password" name="password" placeholder="password">
<span></span>
</div>
<button id="log-in">Log-in</button>
</form>
</html>
<script type="text/javascript">
window.onload = ()=>{
this.sessionStorage.setItem("username", "sakos_userooo");
this.sessionStorage.setItem("password", "sakos_passwordooo");
}

var input = document.getElementsByTagName('input');
var input = document.getElementsById('log-in');
var form = document.querySelector('form');
form.onsubmit = ()=>{return false}

login.onclick = ()=>{
if ((input[0].value != "") && (input[1].value != ""))
{
if ((input[0].value == sessionStorage.setItem("username")) && (input[0].value == sessionStorage.setItem("password")))
{
form.onsubmit = ()=>{return 1}
document.cookie = "username"+input[0].value;
document.cookie = "password"+input[1].value;
}
else
{
if ((input[0].value != sessionStorage.setItem("username")));
{
input[0].nextElementSibling.textContent = "Username NOT match";
setTimeout(()=>{
input[0].nextElementSibling.textContent = "";
}, 2000);
}
if ((input[1].value != sessionStorage.setItem("password")))
{
input[1].nextElementSibling.textContent = "password NOT match";
setTimeout(()=>{
input[1].nextElementSibling.textContent = "";
}, 2000);
}
}
}
else
{
if (input[0].value == "")
{
input[0].nextElementSibling.textContent = "Username is empty";
setTimeout(()=>{
input[0].nextElementSibling.textContent = "";
}, 2000);
}
if (input[0].value == "")
{
input[1].nextElementSibling.textContent = "Password is empty";
setTimeout(()=>{
input[1].nextElementSibling.textContent = "";
}, 2000);
}
}
</script>


