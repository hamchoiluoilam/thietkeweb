<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>English Learning</title>

<style>
body{font-family:Arial;margin:0}

header{
background:#3498db;
color:white;
text-align:center;
padding:15px;
}

.nav{
background:#2ecc71;
padding:10px;
text-align:center;
}

.nav div{
display:inline;
margin:10px;
color:white;
}

.advert{
width:100%;
height:200px;
border:2px solid red;
background:#ffeaa7;
text-align:center;
line-height:200px;
}

.advert:hover{
background:#74b9ff;
border-color:blue;
font-style:italic;
}

.list{
display:flex;
justify-content:center;
flex-wrap:wrap;
}

.item{
width:150px;
height:120px;
background:#74b9ff;
margin:10px;
padding:10px;
color:white;
}

form{
width:50%;
margin:20px auto;
}

input,select{
width:100%;
padding:8px;
margin:5px 0;
}

@media(max-width:1024px){
form{width:70%}
}

@media(max-width:414px){
form{width:90%}
}
</style>
</head>

<body>

<header>
<h1>English Learning</h1>
<p>Learn English Everyday</p>
</header>

<div class="nav">
<div>Home</div>
<div>Course</div>
<div>Contact</div>
</div>

<div class="advert">
Giảm 30% học phí
</div>

<div class="list" id="kq"></div>

<form onsubmit="return check()">

<input type="text" id="name" placeholder="Họ tên">

<input type="email" id="email" placeholder="Email">

<input type="text" id="phone" placeholder="SĐT">

<select>
<option>IELTS</option>
<option>TOEIC</option>
</select>

<input type="text" placeholder="Thời gian học">

<button>Đăng ký</button>

</form>

<script>
let data=`[
{"ten":"IELTS"},
{"ten":"TOEIC"},
{"ten":"Speaking"},
{"ten":"Kids"}
]`;

let a=JSON.parse(data);

let i=0,s="";

while(i<a.length){
s+=`
<div class="item">
<h3>${a[i].ten}</h3>
</div>`;
i++;
}

document.getElementById("kq").innerHTML=s;

function check(){
let n=document.getElementById("name").value;
let e=document.getElementById("email").value;
let p=document.getElementById("phone").value;

if(n==""||e==""||p==""){
alert("Nhập đầy đủ");
return false;
}
}
</script>

</body>
</html>
