<script lang="ts">
  import { createEventDispatcher } from "svelte";
  import Tag from "./Tag.svelte";

  const dispatch = createEventDispatcher<{
    adicionarIngrediente: string;
    removerIngrediente: string;
  }>();

  export let ingrediente: string;

  let selecionado = false;

  function aoClicar() {
    selecionado = !selecionado;

    if (selecionado) {
      dispatch("adicionarIngrediente", ingrediente);
    } else {
      dispatch("removerIngrediente", ingrediente);
    }
  }
</script>

<button on:click={aoClicar}>
  <Tag ativa={selecionado} >{ingrediente}</Tag>
</button>

<style>
  button {
    cursor: pointer;
  }
</style>