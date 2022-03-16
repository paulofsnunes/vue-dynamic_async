<template>
    <div>
        <h1>Contato</h1>
        <input type="text" />
        <!-- abaixo exemplo global -->
        <servicos-empresa />
    </div>
</template>

<script>
import ServicosEmpresa from './ServicosEmpresa.vue';
export default {
  components: { ServicosEmpresa },
    name: "ContatoEmpresa",
};
</script>

<style>
</style>
