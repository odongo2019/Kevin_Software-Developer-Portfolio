```html
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kevin Odongo | Portfolio</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial, Helvetica, sans-serif;
}

body{
background:#f4f6f9;
scroll-behavior:smooth;
}

header{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 60px;
background:#1e3a8a;
position:sticky;
top:0;
z-index:1000;
}

.logo{
color:white;
font-size:24px;
font-weight:bold;
}

nav a{
color:white;
margin-left:20px;
text-decoration:none;
font-size:16px;
transition:0.3s;
}

nav a:hover{
text-decoration:underline;
transform:scale(1.1);
}

section{
padding:70px 80px;
}

h2{
margin-bottom:20px;
color:#1e293b;
}

#about{
text-align:center;
background:white;
}

.profile{
width:150px;
border-radius:50%;
margin-bottom:20px;
}

.social-links{
margin-top:20px;
}

.social-links a{
text-decoration:none;
background:#2563eb;
color:white;
padding:10px 18px;
margin:5px;
border-radius:6px;
display:inline-block;
transition:0.3s;
}

.social-links a:hover{
background:#1e40af;
}

.skill-bar{
margin-bottom:20px;
}

.bar{
width:100%;
background:#ddd;
height:10px;
border-radius:10px;
}

.progress{
height:10px;
border-radius:10px;
animation:load 2s forwards;
}

.html{width:90%;background:#f97316;}
.css{width:85%;background:#2563eb;}
.js{width:75%;background:#facc15;}
.python{width:70%;background:#16a34a;}

@keyframes load{
from{width:0}
}

.project{
background:white;
padding:20px;
border-radius:12px;
margin-bottom:20px;
box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.project-img{
width:100%;
border-radius:8px;
margin-bottom:10px;
}

.recommendation{
background:white;
padding:15px;
border-radius:10px;
margin-bottom:15px;
box-shadow:0 4px 10px rgba(0,0,0,0.1);
font-style:italic;
}

textarea{
width:100%;
height:90px;
padding:10px;
margin-top:10px;
border-radius:6px;
border:1px solid #ccc;
}

button{
margin-top:10px;
padding:10px 20px;
background:#2563eb;
border:none;
color:white;
border-radius:6px;
cursor:pointer;
}

button:hover{
background:#1e40af;
}

.popup{
position:fixed;
top:50%;
left:50%;
transform:translate(-50%,-50%);
background:white;
padding:25px;
border-radius:10px;
box-shadow:0 6px 20px rgba(0,0,0,0.3);
display:none;
text-align:center;
}

.popup button{
margin-top:15px;
}

.home{
position:fixed;
bottom:20px;
right:20px;
font-size:26px;
text-decoration:none;
background:white;
padding:10px;
border-radius:50%;
box-shadow:0 4px 10px rgba(0,0,0,0.3);
}

</style>

<script>

function addRecommendation(){

let text=document.getElementById("newRec").value;

if(text.trim()!=""){

let p=document.createElement("p");
p.className="recommendation";
p.innerText='"'+text+'"';

document.getElementById("recommendation-list").appendChild(p);

document.getElementById("popup").style.display="block";

document.getElementById("newRec").value="";
}

}

function closePopup(){
document.getElementById("popup").style.display="none";
}

</script>

</head>

<body id="top">

<header>

<div class="logo">Kevin Odongo</div>

<nav>
<a href="#about">About</a>
<a href="#skills">Skills</a>
<a href="#projects">Projects</a>
<a href="#recommendations">Recommendations</a>
</nav>

</header>

<section id="about">

<img src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png" class="profile">

<h1>Kevin Odongo</h1>

<p>
A passionate web developer skilled in HTML, CSS, JavaScript and Python.
I enjoy building responsive applications and solving real-world problems
using technology.
</p>

<div class="social-links">
<a href="https://github.com/" target="_blank">GitHub</a>
<a href="https://linkedin.com/" target="_blank">LinkedIn</a>
</div>

</section>

<section id="skills">

<h2>Skills</h2>

<div class="skill-bar">
<p>HTML</p>
<div class="bar"><div class="progress html"></div></div>
</div>

<div class="skill-bar">
<p>CSS</p>
<div class="bar"><div class="progress css"></div></div>
</div>

<div class="skill-bar">
<p>JavaScript</p>
<div class="bar"><div class="progress js"></div></div>
</div>

<div class="skill-bar">
<p>Python</p>
<div class="bar"><div class="progress python"></div></div>
</div>

</section>

<section id="projects">

<h2>Projects</h2>

<div class="project">

<img src="https://via.placeholder.com/400x200" class="project-img">

<h3>Insurance Management System</h3>

<p>
A web platform used by insurance companies to manage policies,
claims and customer information.
</p>

</div>

<div class="project">

<img src="https://via.placeholder.com/400x200" class="project-img">

<h3>Hospital Information System</h3>

<p>
A healthcare system for managing patient records,
appointments and hospital operations.
</p>

</div>

<div class="project">

<img src="https://via.placeholder.com/400x200" class="project-img">

<h3>E-Commerce Web Application</h3>

<p>
An online shopping platform with product catalog,
shopping cart and checkout system.
</p>

</div>

</section>

<section id="recommendations">

<h2>Recommendations</h2>

<div id="recommendation-list">

<p class="recommendation">
"Kevin consistently delivers high-quality work and demonstrates strong technical skills."
</p>

<p class="recommendation">
"A reliable and innovative developer who solves problems effectively."
</p>

<p class="recommendation">
"Great communication skills and excellent teamwork."
</p>

</div>

<h3>Add Recommendation</h3>

<textarea id="newRec" placeholder="Write a recommendation"></textarea>
<br>
<button onclick="addRecommendation()">Submit</button>

</section>

<div id="popup" class="popup">

<p>Thank you. Your recommendation has been submitted.</p>

<button onclick="closePopup()">OK</button>

</div>

<a href="#top" class="home">Home</a>

</body>
</html>
```
