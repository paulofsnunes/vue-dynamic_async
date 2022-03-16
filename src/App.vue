<!-- 
Crie 3 componentes:

1: Componente falando sobre a empresa
2: Componente com os serviços da empresa
3: Componente com um formulário de contato

Crie um menu, que ao clique ele mude os componentes
acima de forma dinâmica. Não destrua o componente
-->
<template>
  <div id="app">
    <!-- <sobre-empresa></sobre-empresa> -->
    <ul>
      <li @click="abaAtiva = 'SobreEmpresa'">Sobre</li>
      <li @click="abaAtiva = 'ServicosEmpresa'">Serviços</li>
      <li @click="abaAtiva = 'ContatoEmpresa'">Contato</li>
    </ul>
    <keep-alive>
      <component :is="abaAtiva"></component>
    </keep-alive>
  </div>
</template>

<script>
import SobreEmpresa from './components/SobreEmpresa.vue';
// import ContatoEmpresa from './components/ContatoEmpresa.vue'
// import ServicosEmpresa from './components/ServicosEmpresa.vue'

export default {
  name: "App",
  components: {
    SobreEmpresa,
    ContatoEmpresa: () => import("./components/ContatoEmpresa.vue")
    // ServicosEmpresa: () => import("./components/ServicosEmpresa.vue")
  },
  data() {
    return {
      abaAtiva: "",
    }
  }
};
</script>

<style>
</style>
