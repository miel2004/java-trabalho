# java-trabalho
<header>

  <div>Reprovador de Alunos Tabajara</div>

</header>

<p>Nota1:
  <input type="text" id="nota1">
</p>
<p>Nota2:
  <input type="text" id="nota2">
</p>
<p>Média:<span id="media"></span></p>
<p>Situação:<span id="situacao"></span></p>

<button onclick="verificaSituacao()">
  Verificar
</button>

<script>

  function verificaSituacao() {

    let n1 = parseFloat(document.getElementById("nota1").value);
    let n2 = parseFloat(document.getElementById("nota2").value);

    let media = (n1 + n2) / 2;
    let situacao = "";
    let cor = "";
    if (media >= 6) {
      situacao = 'Aprovado';
      cor = 'blue';
    } else {
      // && = AND  -   || = OR
      if (media >= 2 && media < 6) {
        situacao = "Exame Final";
        cor = 'orange';
      } else {
        situacao = 'Reprovado';
        cor = 'red';
      }
    }

    document.getElementById("media").innerHTML = media;
    document.getElementById("situacao").innerHTML = situacao;
    document.getElementById("situacao").style.color = cor;

  }

</script>
