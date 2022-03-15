<template>
  <div>
    <Picture />
    <h2>nome: {{ nome }} </h2>
    <p>idade: {{ idade }} </p>
    <p>profissão: {{ profissao }} </p>
    <!-- No P abaixo, conseguimos um link dinamicamente usando o v-bind:href="meu_link" -->
    <p>Meu site é <a target="blank" v-bind:href="meu_link">google.com</a></p>
  </div>
</template>



<script>
import Picture from "./Picture.vue"
export default {
    name: "Pessoa",
    components: {
        Picture
    },
    data() {
        return {
            nome: "Gabriel",
            idade: "30",
            profissao: "programador",
            meu_link: "http://www.google.com"
        };
    },
    components: { Picture }
}
</script>

<style>

</style>
