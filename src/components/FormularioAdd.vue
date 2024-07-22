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

const confirmarsenha = ref("");

const listaEstados = ref([
    { 'nome': 'Acre', 'sigla': 'AC-' },
    { 'nome': 'Alagoas', 'sigla': 'AL-' },
    { 'nome': 'Amapá', 'sigla': 'AP-' },
    { 'nome': 'Amazonas', 'sigla': 'AM-' },
    { 'nome': 'Bahia', 'sigla': 'BA-' },
    { 'nome': 'Ceará', 'sigla': 'CE-' },
    { 'nome': 'Distrito Federal', 'sigla': 'DF-' },
    { 'nome': 'Espírito Santo', 'sigla': 'ES-' },
    { 'nome': 'Goiás', 'sigla': 'GO-' },
    { 'nome': 'Maranhão', 'sigla': 'MA-' },
    { 'nome': 'Mato Grosso', 'sigla': 'MT-' },
    { 'nome': 'Mato Grosso do Sul', 'sigla': 'MS-' },
    { 'nome': 'Minas Gerais', 'sigla': 'MG-' },
    { 'nome': 'Pará', 'sigla': 'PA-' },
    { 'nome': 'Paraíba', 'sigla': 'PB-' },
    { 'nome': 'Paraná', 'sigla': 'PR-' },
    { 'nome': 'Pernambuco', 'sigla': 'PE-' },
    { 'nome': 'Piauí', 'sigla': 'PI-' },
    { 'nome': 'Rio de Janeiro', 'sigla': 'RJ-' },
    { 'nome': 'Rio Grande do Norte', 'sigla': 'RN-' },
    { 'nome': 'Rio Grande do Sul', 'sigla': 'RS-' },
    { 'nome': 'Rondônia', 'sigla': 'RO-' },
    { 'nome': 'Roraima', 'sigla': 'RR-' },
    { 'nome': 'Santa Catarina', 'sigla': 'SC-' },
    { 'nome': 'São Paulo', 'sigla': 'SP-' },
    { 'nome': 'Sergipe', 'sigla': 'SE-' },
    { 'nome': 'Tocantins', 'sigla': 'TO-' },
])

</script>

<template>
    <form>
        <div class="formulario">
            <h1>Preenchas os Campos</h1>
            <div class="nome">
                <label for="perfil.nome">Informe seu nome</label>
                <input v-model="perfil.nome" type="text" min="3" max="30" required>
            </div>
            <div class="email">
                <label for="perfil.email">Informe seu email</label>
                <input v-model="perfil.email" type="text" required>
            </div>
            <div class="senha">
                <label for="perfil.senha">Informe sua senha</label>
                <input v-model="perfil.senha" type="password" required>
            </div>
            <div class="confirmar">
                <label for="confirmarsenha">Confirme sua senha:</label>
                <input v-model="confirmarsenha" type="password" required>
                <p v-if="perfil.senha !== confirmarsenha">Incorreto!</p>
            </div>
            <div class="nascimento">
                <label for="perfil.nascimento">Informe sua data de nascimento</label>
                <input v-model="perfil.nascimento" type="text" required>
            </div>
            <label for="perfil.estado">Informe seu Estado</label>
            <div class="estados">
                <select v-model="perfil.estado">
                    <option v-for="(value, index) of listaEstados" :key="index">{{ value.sigla
                    }}{{ value.nome }}</option>
                </select>
            </div>
            <div class="cidade">
                <label for="perfil.cidade">Informe sua cidade</label>
                <input v-model="perfil.cidade" type="text" required>
            </div>
            <div class="endereco">
                <label fonomer="perfil.endereco">Informe seu endereço</label>
                <input v-model="perfil.endereco" type="text" required>
            </div>
            <div class="hobbies">
                <label for="perfil.hobbies">Informe seu hobbies</label>
                <input v-model="perfil.hobbies" type="text" required>
            </div>
            <div class="linguagem">
                <label for="perfil.linguagem">Informe sua linguagem de programação</label>
                <input v-model="perfil.linguagem" type="text" required>
            </div>
            <label for="perfil.biografia">Escreva sua Biografia</label>
            <div class="biografia">
                <textarea v-model="perfil.biografia" nome="biografia" cols="40" rows="5" required>biografia</textarea>
            </div>
        </div>
        <button @click="$emit('salvar')">Salvar</button>
    </form>
</template>

<style scoped>

</style>