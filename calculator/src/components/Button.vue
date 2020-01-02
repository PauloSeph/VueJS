<template>
<!-- Aqui em :class se double for true ele chama o double e aplica a classe
para esse botão, la em baixo foi definido o CSS com cada classe -->
  <button class="button"
  :class="{ double, tripe, operation }">
      {{ label }}
      {{seinao}}
      
  </button>
</template>

<script>
export default {
    // o componente não tem que ser exportado? O>O
    // Acho que é por causa da pasta components
    data() {
        return {
            lala: "Stringzona"
        }
    },
    

    // Aqui em props está definindo propriedades para o componente, no caso Button.
    // As propriedades só podem ser utilizadas dentro dele.
    // Não são variaveis.
    props: {
        label: {},
        operation: { type: Boolean},
        double: { type: Boolean},
        tripe: { type: Boolean},
        seinao: {
                   }          
        
    }
}
</script>

<style>
/* Definindo variavel */
:root {
    --bg-button: #f0f0f0;
    --border-button: solid 1px #888;
}

.button {
    font-size: 1.4em;
    background-color: var(--bg--button);
    border: none;
    border-right: var(--border-button);
    border-bottom: var(--border-button);
    outline: none;
}
/* Definindo css para os botoes, no caso as classes
as que seram classe como double, tripe, e operation */
.button:active {
    background-color: #ccc
}

.button.double {
    grid-column: span 2;
}

.button.tripe{
    grid-column: span 3;
}

.button.operation {
    background-color: #fa8231;
    color: #fff;
}

.button.operation:active {
    background-color: #fa8231cc
}

</style>