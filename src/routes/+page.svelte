<script>
    const posts = [
      { autor: "João", texto: "Adorei essa rede social!" },
      { autor: "Maria", texto: "Alguém viu o último episódio daquela série incrível?" },
      { autor: "Carlos", texto: "Compartilhando uma foto do meu cachorro!" },
    ];
  </script>
  
  <div>
    <h2>Feed de Postagens</h2>
    {#each posts as post}
      <div class="card my-3">
        <div class="card-body">
          <h5 class="card-title">{post.autor}</h5>
          <p class="card-text">{post.texto}</p>
        </div>
      </div>
    {/each}
  </div>