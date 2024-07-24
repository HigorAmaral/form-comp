<script setup>
import { ref } from 'vue'

const perfil = ref({
    nome: '',
    email: '',
    senha: '',
    nascimento: '',
    estado: '',
    cidade: '',
    endereco: '',
    hobbies: '',
    linguagem: '',
    biografia: '',
})

</script>

<template>
         <div class="resultado">
        <div class="info-results">
        <h2>Dados do Usuario</h2>
        <p>Nome : {{ perfil.nome }}</p>
        <p>Email : {{ perfil.email }}</p>
        <p>Nascimento : {{ perfil.nascimento }}</p>
        <p>Estado : {{ perfil.estado }}</p>
        <p>Cidade : {{ perfil.cidade }}</p>
        <p>Endereço : {{ perfil.endereco }}</p>
        <p>Hobbies : {{ perfil.hobbies }}</p>
        <p>Linguagem : {{ perfil.linguagem }}</p>
        <p>Biografia : {{ perfil.biografia }}</p>
      </div>
        <button class="btn" @click="voltar" >Voltar</button>
      </div>
</template>

<style scoped></style>