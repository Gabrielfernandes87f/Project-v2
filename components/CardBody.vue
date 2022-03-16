<template>
  <div id="CardBody">
    <p>Gabriel fernandes</p>
    <p>Saudação: {{ message }}</p>

    <button @click="ShowEmail">{{ textoBotao }}</button>

    <p v-show="mostrar_email">Meu email é: {{ email }}</p>

    <ul>
      <li v-for="(list, index) in techs" v-bind:key="index">{{ list }}</li>
    </ul>

    <ul>
      <li v-for="(pro, index) in professions" v-bind:key="index">
        <!--  {{ pro.name }} :{{ pro.description }} -->

        <!-- Nome do banco: {{ pro.banco.name }} Agencia: {{ pro.banco.agencia }} -->
        Nome: {{ pro.person.name }}
      </li>
    </ul>
    <ul>
      <li v-for="couse in couses" :key="couse.id">cursos em andamento: {{ couse.name }}</li>
    </ul>
  </div>
</template>
<style scoped>
button {
  background-color: rgb(87, 8, 8);
  color: #fff;
  padding: 10px;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  margin: 10px 0;
}
#CardBody {
  background-color: #b56325;
  color: #5eff00;
}
</style>

<script>
export default {
  name: 'CardBody',
  data() {
    return {
      message: "Seja bem vindo ao vue",
      mostrar_email: false,
      email: "gabriel@gmail.com.br",
      textoBotao: "Mostrar email",
      techs: [
        "HTML", "CSS", "JS"
      ],

      professions: [
        {
          name: "Programador",
          banco:
          {
            name: "Banco do Brasil",
            agencia: "34234"
          },
          person: [
            {
              name: "Gabriel",
              age: "23"
            },
            {
              name: "João",
              age: "24"
            }
          ]
        }
      ],
      couses: [
        { id: 1, name: "Vue.js" },
        { id: 2, name: "Nuxt.js" },
        { id: 3, name: "Microservices" }
      ]

    }
  },
  created() {
    setTimeout(() => {
      this.lifeCycle()
    }, 3000)
  },
  props: {
    mostrar_email: {
      type: Boolean,
      required: true
    }
  },
  methods: {
    ShowEmail() {
      this.mostrar_email = !this.mostrar_email
      if (!this.mostrar_email) {
        this.textoBotao = "mostrar email"
        console.log("mostrar email")
      } else {

        this.textoBotao = "esconder email"

      }

    },
    lifeCycle() {
      console.log("lifeCycle")
    }
  }

}

</script>
