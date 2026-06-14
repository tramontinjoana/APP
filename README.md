<!DOCTYPE html>
<html>
<head>
    <title>Login - StudyApp</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

<div class="container">

<h1>StudyApp</h1>

<input type="text" id="usuario" placeholder="Usuário">

<input type="password" id="senha" placeholder="Senha">

<button onclick="login()">Entrar</button>

<p id="erro"></p>

</div>


<script src="script.js"></script>

</body>
</html>
<!DOCTYPE html>
<html>

<head>

<title>Home - Estudos</title>

<link rel="stylesheet" href="style.css">

</head>


<body>


<header>

<h1>📚 Minha Área de Estudos</h1>

<a href="logout.html">
Sair
</a>

</header>



<div class="cards">


<div class="card">

<h2>🔗 Links de Estudo</h2>

<ul>

<li>
<a href="https://www.youtube.com" target="_blank">
Video aulas
</a>
</li>


<li>
<a href="https://www.khanacademy.org" target="_blank">
Khan Academy
</a>
</li>


<li>
<a href="https://www.alura.com.br" target="_blank">
Cursos
</a>
</li>

</ul>

</div>




<div class="card">

<h2>📝 Notas</h2>


<textarea placeholder="Digite suas anotações..."></textarea>


</div>




<div class="card">


<h2>📅 Cronograma</h2>


<table>

<tr>
<th>Dia</th>
<th>Matéria</th>
</tr>


<tr>
<td>Segunda</td>
<td>Matemática</td>
</tr>


<tr>
<td>Terça</td>
<td>Programação</td>
</tr>


<tr>
<td>Quarta</td>
<td>Banco de Dados</td>
</tr>


</table>


</div>



</div>
<!DOCTYPE html>

<html>

<head>

<title>Logout</title>

<link rel="stylesheet" href="style.css">

</head>


<body>


<div class="container">


<h1>Você saiu!</h1>


<p>Obrigado por estudar conosco.</p>


<a href="index.html">

Voltar ao Login

</a>


</div>


<script>

localStorage.removeItem("usuario");

</script>


</body>

</html>
function login(){


let usuario =
document.getElementById("usuario").value;


let senha =
document.getElementById("senha").value;



if(usuario=="aluno" && senha=="1234"){


localStorage.setItem(
"usuario",
usuario
);


window.location.href="home.html";


}

else{


document.getElementById("erro")
.innerHTML="Usuário ou senha incorretos";


}


}
body{

font-family: Arial;

background:#eef2f7;

margin:0;

}



.container{

width:350px;

margin:100px auto;

background:white;

padding:30px;

border-radius:15px;

box-shadow:0 0 10px #aaa;

text-align:center;

}



input, textarea{

width:90%;

padding:10px;

margin:10px;

}



button{

background:#2563eb;

color:white;

border:none;

padding:12px;

width:100%;

border-radius:8px;

}



header{

background:#2563eb;

color:white;

padding:20px;

display:flex;

justify-content:space-between;

}



.cards{

display:flex;

gap:20px;

padding:30px;

}



.card{

background:white;

padding:20px;

border-radius:15px;

width:30%;

box-shadow:0 0 10px #bbb;

}



table{

width:100%;

}



th,td{

border:1px solid #ccc;

padding:8px;

}



a{

text-decoration:none;

color:#2563eb;

}


#erro{

color:red;

}

</body>

</html>
