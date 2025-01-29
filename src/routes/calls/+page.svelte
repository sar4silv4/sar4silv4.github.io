<script>
  const notificacoes = [
    { tipo: "Curtir", mensagem: "João curtiu sua postagem." },
    { tipo: "Comentário", mensagem: "Maria comentou na sua postagem." },
    { tipo: "Seguidor", mensagem: "Carlos começou a te seguir." },
    { tipo: "Republicar", mensagem: "Ana republicou sua postagem." },
 
  ];
</script>

<div>
  <h2>Notificações</h2>
  {#each notificacoes as notificacao}
    <div class="alert alert-info">
      <strong>{notificacao.tipo}:</strong> {notificacao.mensagem}
    </div>
  {/each}
</div>