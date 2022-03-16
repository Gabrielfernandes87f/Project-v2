<template>
  <div>
    <form action @submit="SubimitForm($event)">
      <input type="text" v-model="nome" />
      <input type="text" v-model="email" />

      <input id="submit" type="submit" value="enviar" />
    </form>
    <p>{{ emailProps }}</p>
  </div>
</template>
<style>
#submit {
  background-color: rgb(87, 8, 8);
  color: #fff;
  padding: 10px;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  margin: 10px 0;
}
</style>

<script >
export default {
  name: 'Form',
  data() {
    return {
      nome: "",
      email: ""

    }
  },
  props: {
    emailProps: {
      type: String,
      required: true
    },
    inputColor: {
      type: String,
      required: true
    },
    inputName: {
      type: String,
      required: true
    }

  },
  methods: {
    SubimitForm(e) {
      e.preventDefault();
      console.log(" nome: " + this.nome + " email: " + this.email);

    }
  }
}
</script>

