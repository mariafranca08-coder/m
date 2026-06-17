<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Minha Netflix</title>

<style>
body{
margin:0;
background:#141414;
color:white;
font-family:Arial;
}

header{
position:fixed;
top:0;
width:100%;
background:rgba(0,0,0,0.9);
display:flex;
justify-content:space-between;
padding:15px 30px;
z-index:10;
}

.logo{
color:#e50914;
font-size:28px;
font-weight:bold;
}

nav a{
color:white;
margin-left:20px;
text-decoration:none;
}

/* 🎬 BANNER ESTILO NETFLIX REAL */
.banner{
position:relative;
width:100%;
height:90vh;
margin-top:60px;
overflow:hidden;
}

.banner iframe{
position:absolute;
top:0;
left:0;
width:100%;
height:100%;
border:none;
}

.banner::after{
content:"";
position:absolute;
bottom:0;
left:0;
width:100%;
height:40%;
background:linear-gradient(to top, #141414, transparent);
}

.title{
position:absolute;
bottom:30px;
left:30px;
font-size:28px;
z-index:2;
}

.section{
padding:20px;
}

.row{
display:flex;
gap:10px;
overflow-x:auto;
}

.thumb{
width:180px;
height:100px;
background:#333;
border-radius:6px;
flex-shrink:0;
cursor:pointer;
transition:0.2s;
background-size:cover;
}

.thumb:hover{
transform:scale(1.05);
}
</style>
</head>

<body>

<header>
<div class="logo">MINHAFLIX</div>
<nav>
<a href="#">Início</a>
<a href="#">Filmes</a>
<a href="#">Séries</a>
</nav>
</header>

<!-- 🎬 FILME EM DESTAQUE REAL -->
<div class="banner">

<iframe
src="https://www.youtube.com/embed/Og-N4WaGRMU?autoplay=1&mute=1"
allowfullscreen>
</iframe>

<div class="title">Filme em destaque</div>

</div>

<!-- 🎞️ LISTA -->
<div class="section">
<h2>Mais filmes</h2>

<div class="row">

<div class="thumb"
style="background-image:url('https://img.youtube.com/vi/Og-N4WaGRMU/hqdefault.jpg');"
onclick="document.querySelector('iframe').src='https://www.youtube.com/embed/Og-N4WaGRMU?autoplay=1&mute=1'">
</div>

<div class="thumb"></div>
<div class="thumb"></div>
<div class="thumb"></div>

</div>

</div>

</body>
</html>