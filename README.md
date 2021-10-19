- Script javaScript
```bash
const calcular = document.getElementById("calcular");

function imc() {
  const nome = document.getElementById("nome").value;
  const altura = document.getElementById("altura").value;
  const peso = document.getElementById("peso").value;
  const resultado = document.getElementById("resultado");

  if (nome !== "" && altura !== "" && peso !== "") {
    const valorImc = (peso / (altura * altura)).toFixed(2);

    let classificacao = "";

    if (valorImc < 18.5) {
      classificacao = " abaixo do peso.";
    }

    if (valorImc > 18.5 && valorImc < 25) {
      classificacao = " com peso ideal. Parabéns!!!";
    }

    if (valorImc > 25 && valorImc < 30) {
      classificacao = " levemente acima do peso";
    }

    if (valorImc > 30 && valorImc < 35) {
      classificacao = " com obesidade grau I";
    }

    if (valorImc > 35 && valorImc < 40) {
      classificacao = " com obesidade grau II";
    }

    if (valorImc > 40) {
      classificacao = " com obesidade grau III. Cuidado!!!";
    }

    resultado.textContent = `${nome} seu IMC  é ${valorImc} e você está ${classificacao}`;

  } else {
    resultado.textContent = "Preencha todos os campos !!!";
  }
}

calcular.addEventListener("click", imc);
```


- Html IMC
```bash
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IMC</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <main>
      <div class="container">
        <div class="title"> Calculadora - IMC </div>
        <div class="input">
            <label>Nome:</label>
            <input type="text" id='nome'>
        </div>
        <div class="input">
            <label>Altura:</label>
            <input type="number" id='altura'>
        </div>
        <div class="input">
            <label>Peso:</label>
            <input type="number" id='peso'>
        </div>
        <button id='calcular'>Calcular</button>

        <div class="result" id='resultado'></div>
      </div>
    </main>
    <script src="./imc.js"></script>
  </body>
</html>

calcular.addEventListener("click", imc);
```


- Script CSS
```bash
main{
    display: flex;
    width: 100vw;
    height: 100vh;
    justify-content: center;
    align-items: center;
  
  }
  
  .container{
    display: flex;
    flex-direction: column;
    background: rgb(255,198,0);
    width: 400px;
    height: 600px;
    align-items: center;
    justify-content: space-evenly;
    border-radius: 20px;
    box-shadow: 0 0 10px black;
  }
  
  .title{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 50px;
    font: bold 2.5rem serif;
    border-bottom: solid 5px black;
    margin-bottom: 20px;
  }
  
  .input {
    display: flex;
    width: 300px;
    height: 50px;
    justify-content: space-between;
    align-items: center;
  }
  .input input {
    width: 200px;
    height: 50px;
    border-radius: 5px;
    border:none;
    outline: 0;
    font: bold 1.5rem serif;
    text-align: center;
  }
  
  .input label {
    font: bold 1.5rem serif;
  }
  
  button{
    width: 300px;
    height: 40px;
    font: bold 1.2rem serif;
    background: #000;
    color: rgb(255,198,0);
    outline: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .result{
    display: flex;
    margin-top: 20px;
    align-items: center;
    width: 300px;
    height: 150px;
    border-radius: 5px;
    font: italic 1.5rem serif;
    box-shadow: 0px 0px 10px black;
    background: #000;
    color: rgb(255,198,0);
    padding: 20px;
    box-sizing: border-box;
    user-select: none;
  }
```
<h1>
<img src="https://github.com/Maksuedson/assets/blob/master/java-script/page-imc.PNG">

</h1>
