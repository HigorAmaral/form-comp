<script setup>
import FormularioAdd from './components/FormularioAdd.vue';
import FormularioResp from './components/FormularioResp.vue';

</script>

<template>
<formulario-add v-if="!mostarResultado" />
<formulario-resp v-if="mostarResultado" />

</template>

<style scoped>

</style>
