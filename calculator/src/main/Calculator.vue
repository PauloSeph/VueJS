<template>
  <div class="calculator">
      <Display/>
      <Button label="AC" triple/>
      <Button label="/"/>
      <Button label="7"/>
      <Button label=""/>
      <Button label=""/>
      <Button label=""/>
      <Button label=""/>
      <Button label=""/> 
      <Button label=""/>
      <Button label=""/>
      <Button label=""/>
      <Button label=""/>
      <Button label=""/>
      <Button label=""/>
      <!-- Aqui nao consegue acessar a variavel definida em data do arquivo do componente Button.vue -->
      {{lala}}
    <!-- A propriedade(props) é dentro do Button -->

    <Button seinao="aa"></Button>
    <!-- Dessa forma não é possivel.
    Tem que usar o  </slot> para associar-->
    <Button>{{seinao}}</Button>
  </div>
</template>

<script>
import Display from "../components/Display"
import Button from "../components/Button"

export default {
    components: { Button, Display }
}
</script>

<style>
    .calculator {
        height: 320px;
        width: 235px;
        border-radius: 5px;
        overflow: hidden;

        display: grid;
        grid-template-columns: repeat(4, 25%);
        grid-template-rows: 1fr 48px 48px 48px 48px 48px;
        
    }
</style>