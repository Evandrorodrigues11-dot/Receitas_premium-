<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Receitinhas_da_Tia_Ana</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:linear-gradient(rgba(0,0,0,.7),rgba(0,0,0,.7)),
url('https://images.unsplash.com/photo-1578985545062-69928b1d9587?auto=format&fit=crop&w=1600&q=80');
background-size:cover;
background-position:center;
background-attachment:fixed;
color:white;
}

header{
text-align:center;
padding:30px 15px;
}

.logo{
width:100px;
height:100px;
border-radius:50%;
background:white;
color:#d35400;
display:flex;
align-items:center;
justify-content:center;
font-size:45px;
margin:auto;
margin-bottom:15px;
}

header h1{
font-size:32px;
}

header p{
opacity:.8;
margin-top:5px;
}

.total{
width:90%;
max-width:500px;
margin:15px auto;
background:#25D366;
padding:15px;
border-radius:12px;
text-align:center;
font-size:22px;
font-weight:bold;
}

.catalogo{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(170px,1fr));
gap:15px;
padding:15px;
padding-bottom:120px;
}

.card{
background:white;
border-radius:15px;
overflow:hidden;
box-shadow:0 5px 15px rgba(0,0,0,.4);
}

.card img{
width:100%;
height:170px;
object-fit:cover;
}

.card-body{
padding:12px;
color:#222;
}

.card-body h3{
font-size:15px;
margin-bottom:8px;
}

.preco{
color:#d35400;
font-size:20px;
font-weight:bold;
margin-bottom:10px;
}

.btn{
width:100%;
padding:10px;
border:none;
background:#25D366;
color:white;
font-weight:bold;
border-radius:8px;
cursor:pointer;
}

footer{
position:fixed;
bottom:0;
left:0;
width:100%;
background:white;
padding:10px;
}

.finalizar{
width:100%;
padding:15px;
border:none;
background:#d35400;
color:white;
font-size:18px;
font-weight:bold;
border-radius:10px;
cursor:pointer;
}

.whatsapp{
position:fixed;
right:20px;
bottom:85px;
width:65px;
height:65px;
background:#25D366;
border-radius:50%;
display:flex;
align-items:center;
justify-content:center;
text-decoration:none;
box-shadow:0 5px 15px rgba(0,0,0,.4);
}

.whatsapp img{
width:38px;
}
</style>
</head>

<body>

<header>
<div class="logo">🎂</div>
<h1>Receitinhas_da_Tia_Ana</h1>
<p>Receitas Premium de Bolos</p>
</header>

<div class="total">
Total: <span id="total">0</span> Kz
</div>

<div class="catalogo">

<div class="card">
<img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Red Velvet</h3>
<div class="preco">3000 Kz</div>
<button class="btn" onclick="adicionar('Receita Red Velvet',3000)">Comprar Receita</button>
</div>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1551024506-0bccd828d307?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Naked Cake</h3>
<div class="preco">2500 Kz</div>
<button class="btn" onclick="adicionar('Receita Naked Cake',2500)">Comprar Receita</button>
</div>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1606313564200-e75d5e30476c?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Chocolate Premium</h3>
<div class="preco">2800 Kz</div>
<button class="btn" onclick="adicionar('Receita Chocolate Premium',2800)">Comprar Receita</button>
</div>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1603532648955-039310d9ed75?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Bolo de Abacaxi</h3>
<div class="preco">2200 Kz</div>
<button class="btn" onclick="adicionar('Receita Bolo de Abacaxi',2200)">Comprar Receita</button>
</div>
</div>

</div>

<a class="whatsapp"
href="https://wa.me/244924887853"
target="_blank">
<img src="https://cdn-icons-png.flaticon.com/512/733/733585.png">
</a>

<footer>
<button class="finalizar" onclick="finalizarCompra()">
🛒 Finalizar Compra
</button>
</footer>

<script>

let carrinho = [];
let total = 0;

function adicionar(nome,preco){

carrinho.push({
nome:nome,
preco:preco
});

total += preco;

document.getElementById("total").innerText = total;

alert(nome + " adicionada ao carrinho!");
}

function finalizarCompra(){

if(carrinho.length === 0){
alert("Escolha pelo menos uma receita.");
return;
}

let mensagem =
"Olá! Quero comprar as seguintes receitas:%0A%0A";

for(let i=0;i<carrinho.length;i++){
mensagem +=
"• " +
carrinho[i].nome +
" - " +
carrinho[i].preco +
" Kz%0A";
}

mensagem +=
"%0A💰 Total: " +
total +
" Kz";

window.open(
"https://wa.me/244924887853?text=" + mensagem,
"_blank"
);

}

</script>

</body>
</html><div class="card">
<img src="https://images.unsplash.com/photo-1519869325930-281384150729?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Bolo de Maracujá</h3>
<div class="preco">2400 Kz</div>
<button class="btn" onclick="adicionar('Receita Bolo de Maracujá',2400)">Comprar Receita</button>
</div>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1606313564200-e75d5e30476c?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Bolo de Chocolate Fudge</h3>
<div class="preco">3000 Kz</div>
<button class="btn" onclick="adicionar('Receita Bolo de Chocolate Fudge',3000)">Comprar Receita</button>
</div>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1627308595229-7830a5c91f9f?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Bolo de Amêndoa</h3>
<div class="preco">2600 Kz</div>
<button class="btn" onclick="adicionar('Receita Bolo de Amêndoa',2600)">Comprar Receita</button>
</div>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1562440499-64c9a111f713?auto=format&fit=crop&w=900&q=80">
<div class="card-body">
<h3>Receita Bolo de Doce de Leite</h3>
<div class="preco">2900 Kz</div>
<button class="btn" onclick="adicionar('Receita Bolo de Doce de Leite',2900)">Comprar Receita</button>
</div>
</div>
