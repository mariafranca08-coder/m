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

/* HEADER */
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

/* BANNER */
.banner{
position:relative;
width:100%;
height:85vh;
margin-top:60px;
background:black;
}

.banner iframe{
position:absolute;
width:100%;
height:100%;
top:0;
left:0;
border:none;
}

.title{
position:absolute;
bottom:30px;
left:30px;
font-size:26px;
z-index:2;
}

/* LISTA */
.section{
padding:20px;
}

.row{
display:flex;
gap:12px;
overflow-x:auto;
padding-bottom:10px;
}

/* CAPAS */
.thumb{
width:160px;
height:240px;
background-size:cover;
background-position:center;
border-radius:8px;
flex-shrink:0;
cursor:pointer;
transition:0.2s;
}

.thumb:hover{
transform:scale(1.07);
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

<!-- 🎬 DESTAQUE -->
<div class="banner">
<iframe id="videoPlayer"
src="https://www.youtube.com/embed/Og-N4WaGRMU?autoplay=1&mute=1"
allow="autoplay; encrypted-media"
allowfullscreen>
</iframe>

<div class="title">Filme em destaque</div>
</div>

<!-- 🎞️ FILMES -->
<div class="section">
<h2>Mais filmes</h2>

<div class="row">

<!-- Frozen -->
<div class="thumb"
style="background-image:url('https://image.tmdb.org/t/p/w500/6ApDtO7xaWAfPqfi2IARXIzj8QS.jpg');"
onclick="changeVideo('dQw4w9WgXcQ')">
</div>

<!-- Shrek -->
<div class="thumb"
style="background-image:url('https://image.tmdb.org/t/p/w500/iB64vpL3dIObOtMZgX3RqdVdQDc.jpg');"
onclick="changeVideo('kxopViU98Xo')">
</div>

<!-- Bela e a Fera -->
<div class="thumb"
style="background-image:url('https://image.tmdb.org/t/p/w500/7oCAPOphDKpIAX0iJk.jpg');"
onclick="changeVideo('9bZkp7q19f0')">
</div>

<!-- Toy Story -->
<div class="thumb"
style="background-image:url('https://image.tmdb.org/t/p/w500/uXDfjJbdP4ijW5hWSBrPrlKpxab.jpg');"
onclick="changeVideo('Og-N4WaGRMU')">
</div>

</div>
</div>

<script>
function changeVideo(id){
document.getElementById("videoPlayer").src =
"https://www.youtube.com/embed/" + id + "?autoplay=1&mute=1&rel=0";
}
</script>

</body>
</html>