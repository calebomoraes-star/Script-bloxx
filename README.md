<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Promoções EB</title>
</head>
<body style="background:#0f172a;color:white;text-align:center;font-family:Arial;">

  <h1 style="color:#22c55e;">Exército Brasileiro RP</h1>

  <input id="nome" placeholder="Nome do jogador"><br><br>

  <select id="patente">
    <option>Soldado</option>
    <option>Cabo</option>
    <option>Sargento</option>
    <option>Tenente</option>
    <option>Capitão</option>
  </select><br><br>

  <button onclick="promover()">Promover</button>

  <div id="log"></div>

  <script>
    function promover(){
      let nome = document.getElementById('nome').value;
      let patente = document.getElementById('patente').value;

      if(!nome){
        alert('Digite o nome');
        return;
      }

      let log = document.getElementById('log');
      let p = document.createElement('p');
      p.innerText = nome + ' promovido para ' + patente;

      log.appendChild(p);
    }
  </script>

</body>
</html>
