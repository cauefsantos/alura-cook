<script>
  import Card from "../../compartilhados/Card.svelte";
</script>

<Card>
  <img class="receita-img" src="/imagens/receitas/alho_assado.png" alt="Alho assado">

  <div class="receita-info">
    <h3 class="receita-nome">Alho assado</h3>
  </div>
</Card>

<style>
  .receita-img {
    width: 100%;
    height: 150px;
  }

  .receita-nome {
    font-size: 1.125rem;
  }

  .receita-info {
    padding: 0.75rem 0.875rem;
  }
</style>