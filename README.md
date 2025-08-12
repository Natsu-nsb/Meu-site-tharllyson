# Meu-site-tharllyson
Meu site para teste
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Troll App</title>
<style>
    body {
        margin: 0;
        background: #f0f0f0;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        font-family: Arial, sans-serif;
    }
    #container {
        text-align: center;
    }
    button {
        padding: 15px 30px;
        font-size: 20px;
        border: none;
        border-radius: 10px;
        background-color: #4CAF50;
        color: white;
        cursor: pointer;
        transition: background 0.3s;
        position: absolute;
    }
    button:hover {
        background-color: #45a049;
    }
    #mensagem {
        display: none;
        font-size: 24px;
        color: red;
    }
</style>
</head>
<body>

<div id="container">
    <button id="botao">Começar</button>
    <div id="mensagem">Você é idiota 😂</div>
</div>

<script>
const botao = document.getElementById("botao");
const mensagem = document.getElementById("mensagem");
let cliques = 0;

function moverBotao() {
    const larguraTela = window.innerWidth - 150;
    const alturaTela = window.innerHeight - 70;
    const novaX = Math.random() * larguraTela;
    const novaY = Math.random() * alturaTela;
    botao.style.left = `${novaX}px`;
    botao.style.top = `${novaY}px`;
}

botao.addEventListener("click", () => {
    cliques++;
    if (cliques < 5) {
        moverBotao();
    } else {
        botao.style.display = "none";
        mensagem.style.display = "block";
    }
});

// Posição inicial centralizada
botao.style.left = `${(window.innerWidth / 2) - 75}px`;
botao.style.top = `${(window.innerHeight / 2) - 35}px`;
</script>

</body>
</html>
