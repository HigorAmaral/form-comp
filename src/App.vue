<script setup>
import { ref } from 'vue'
import FormularioAdd from './components/FormularioAdd.vue';
import FormularioResp from './components/FormularioResp.vue';
const mostarResultado = ref(true)

const nome = ref(null)
const email = ref(null)
const senha = ref(null)
const nascimento = ref(null)
const estado = ref(null)
const cidade = ref(null)
const endereco = ref(null)
const hobbies = ref(null)
const linguagem = ref(null)
const biografia = ref(null)

function passarDados(perfil) {
    nome.value = perfil.nome
    email.value = perfil.email
    senha.value = perfil.senha
    nascimento.value = perfil.nascimento
    estado.value = perfil.estado
    cidade.value = perfil.cidade
    endereco.value = perfil.endereco
    hobbies.value = perfil.hobbies
    linguagem.value = perfil.linguagem
    biografia.value = perfil.biografia

    mostarResultado.value = !mostarResultado.value
}


</script>

<template>
    <formulario-add @perfil="passarDados" v-if="mostarResultado" />
    <formulario-resp :nome="nome" :email="email" :senha="senha" :nascimento="nascimento" :estado="estado"
        :cidade="cidade" :endereco="endereco" :hobbies="hobbies" :linguagem="linguagem" :biografia="biografia"
        @voltar="mostarResultado = !mostarResultado" v-else></formulario-resp>

</template>

<style scoped></style>
