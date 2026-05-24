----câu 1 ---
<!DOCTYPE html>
<html lang = "vn">
<head>
<meta charset="utf-8">
<title>English Learning</title>
<style>
body{font-family:Arial;margin:0}
header{background:#3498db;color:white;text-align:center;padding:15px}
.nav{background:#2ecc71;padding:10px;text-align:center}
.nav div{display:inline;margin:10px;color:white}
article{padding:20px}
</style>
</head>

<body>

<header>
<svg width="50" height="50">
<circle cx="25" cy="25" r="20" fill="red"/p>
</svg>
<h1>English Learning</h1>
</header>

<div class="nav">
<div>Home</div>
<div>Course</div>
<div>Contact</div>
</div>

<article>
<h2>IELTS Course</h2>
<img src="https://picsum.photos/300/150">
<p><strong>IELTS Basic</strong> dành cho sinh viên.</p>
</article>

</body>
</html>


-----câu 2------
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
.item{
width:150px;
height:100px;
background:#74b9ff;
margin:5px;
display:inline-block;
}

.advert{
width:100%;
height:200px;
border:2px solid red;
background:#ffeaa7;
}
</style>
</head>

<body>

<div class="item"></div>
<div class="item"></div>
<div class="item"></div>
<div class="item"></div>

<div class="advert"></div>

</body>
</html>



-----câu 3----
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<style>
div{border:1px solid gray;margin:10px;padding:10px}
</style>
</head>

<body>

<p id="kq"></p>

<script>
let data=`[
{"ten":"IELTS","hocphi":"3tr"},
{"ten":"TOEIC","hocphi":"2tr"},
{"ten":"Speaking","hocphi":"1tr"},
{"ten":"Kids","hocphi":"1.5tr"}
]`;

let a=JSON.parse(data);

let i=0,s="";

while(i<a.length){
s+=`
<div>
<h3>${a[i].ten}</h3>
<p>${a[i].hocphi}</p>
</div>`;
i++;
}

document.getElementById("kq").innerHTML=s;
</script>

</body>
</html>


-----câu 4-----
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>cau4</title>

<style>
body{font-family:Arial}

@media(max-width:414px){
form{width:95%}
}

@media(min-width:415px) and (max-width:1024px){
form{width:70%}
}

@media(min-width:1440px){
form{width:50%}
}
</style>
</head>

<body>

<form onsubmit="return check()">

<h2>Đăng ký khóa học</h2>

<input type="text" id="name" placeholder="Họ và tên">

<input type="email" id="email" placeholder="Email">

<input type="text" id="phone" placeholder="Số điện thoại">

<select id="course">
<option value="">Chọn khóa học</option>
<option>IELTS</option>
<option>TOEIC</option>
</select>

<input type="text" id="time" placeholder="Thời gian học">

<button>Đăng ký</button>

</form>

<script>
function check(){

if(name.value==""){
alert("Nhập họ tên");
return false;
}

if(email.value==""){
alert("Nhập email");
return false;
}

if(phone.value==""){
alert("Nhập số điện thoại");
return false;
}

return true;
}
</script>

</body>
</html>

----Câu 5-----
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
