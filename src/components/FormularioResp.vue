<script setup>

defineProps({
  nome:String,
  email:String,
  senha:String,
  nascimento:Date,
  estado:String,
  cidade:String,
  endereco:String,
  hobbies:String,
  linguagem:String,
  biografia:String
})

</script>

<template>
         <div class="resultado">
        <div class="info-results">
        <h2>Dados do Usuario</h2>
        <p>Nome : {{ nome }}</p>
        <p>Email : {{ email }}</p>
        <p>Nascimento : {{ nascimento }}</p>
        <p>Estado : {{ estado }}</p>
        <p>Cidade : {{ cidade }}</p>
        <p>Endereço : {{ endereco }}</p>
        <p>Hobbies : {{ hobbies }}</p>
        <p>Linguagem : {{ linguagem }}</p>
        <p>Biografia : {{ biografia }}</p>
      </div>
        <button class="btn" @click="voltar" >Voltar</button>
      </div>
</template>

<style scoped></style>