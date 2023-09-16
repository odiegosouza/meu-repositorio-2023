<!DOCTYPE html>
<html>
<head>
    <title>Soundlike</title>
</head>
<body>
  <h2>Crie aqui sua Playlist</h2>
  <span>Prazer, qual é o seu nome?</span><br>
  <input type="text" id="input_nome"><br>
  <span>Qual o nome da Playlist?</span><br>
  <input type="text" id="input_playlist"><br>
  <span>Digite uma musica:</span><br>
  <input type="text" id="input_musica"><br>
  <span>Qual é o cantor(a):</span><br>
  <input type="text" id="input_cantor"><br>
  <button onclick="calcular()">Clique aqui</button>
  <div id="exibir"></div>
</body>
</html>
<script>

var musica = ""
var playlist = ""

function calcular(){
  var nome = input_nome.value;
  playlist = input_playlist.value;
  musica = input_musica.value
  var cantor = input_cantor.value;


  exibir.innerHTML = `
  Olá, ${nome}! Tem certeza que deseja adicionar a música "${musica}" de ${cantor}, na Playlist ${playlist}? <br>
  
  <button onclick="adicionar()">adicione</button>
  <button onclick="apagar()">Cancelar</button>`
    
  }

  function adicionar(){
    exibir.innerHTML += `<br>Legal, "${musica}" foi adicionada na playlist ${playlist} :)
    <br>
    <button onclick="adicionarmore()">Adicionar Mais</button>
    <button onclick="cancelar()">Encerrar</button>`
    
  }

  function apagar(){
    exibir.innerHTML +=` <br>Ok, música "${musica}" não foi adicionada!`
  }

  function cancelar(){
    exibir.innerHTML += `<br>Música foi adicionada e o processo foi encerrado.`

  }
  function adicionarmore(){

    exibir.innerHTML += `
    
    <h2>Adicione mais músicas </h2>
  
    <span>Em qual Playlist deseja adicionar?</span><br>
    <input type="text" id="playlist"><br>
    <span>Digite uma musica:</span><br>
    <input type="text" id="music"><br>
    <span>Qual é o cantor(a):</span><br>
    <input type="text" id="cantortodos"><br>

    <button onclick="adicionarmais()">Adicionar</button>`
  }
 
  function adicionarmais(){
   exibir.innerHTML += `<br>Música adicionada com sucesso, até mais! :)`

  }



</script>
