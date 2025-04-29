<!-- 
• Este projeto será uma calculadora aritmética;

• Deverá conter dois campos para inserir os números;

• Um campo do tipo select para escolher a operação aritmética;

• Ao alterar os valores o cálculo já deverá ser realizado, sem precisar clicar em nenhum botão; 
-->

<template>
  <div class="container">
    <TheHeader/>
    
    <OperandsForms/>

    </div>
</template>

<script>
  import TheHeader from './components/TheHeader.vue';
  import OperandsForms from './components/OperandsForms.vue';

  export default {
    name: 'App',
    components: { TheHeader, OperandsForms },
  }

</script>
