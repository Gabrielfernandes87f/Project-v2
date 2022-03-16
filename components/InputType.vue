<template>
  <div>
    <h1>
      minha profissão é: {{ profissao }}
    </h1>
    <p v-if="esta_trabalhando">
      Estou trabalhando.</p>
    <p v-else>
      Estou disponivel para trabalho.</p>
    <p v-show="mostrar_email">
      Meu email é: {{ email }}
    </p>


  </div>
</template>

<script>


export default {
  name: 'InputType',
  data() {
    return {
      profissao: 'ainda nao sei',
           // se essa function for true, o pai vai renderizar o filho (v-if e v-else)
     esta_trabalhando: true,
     // essa condiçao mostrar ou nao mostra. (v-show)
     mostrar_email: true,
     email: 'gabriel@gmail.com'
    }
 },
 created() {
   setTimeout(() => {
     this.profissao = 'programador'
    }, 2000)

 },
 mounted() {
   setTimeout(() => {
     this.profissao = 'fullstack'
    }, 4000)
 }

}
</script>
