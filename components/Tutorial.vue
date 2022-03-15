<!-- Please remove this file from your project -->
<template>
  <div class="text-center justify-center text-base max-h-fit pt-20">
    <h1>Olá Vue</h1>
    <div>
      {{ desc }}
    </div>
    <div class>
      <CardBody />
    <div>
     <InputType />
    </div>
    <div>
      <Pessoa />
    </div>
    </div>
  </div>
</template>

<script>
import CardBody from './CardBody'
import InputType from './InputType'
import Pessoa from './Pessoa'
export default {
  name: 'NuxtTutorial',
  components: {
    CardBody,
    InputType,
    Pessoa
  },
  data() {
    return {
      desc: 'Vue.js é uma biblioteca JavaScript de código aberto, desenvolvida pelo Vue.js Team, que permite a criação de interfaces de usuário através de componentes reutilizáveis.'
    }
  }
}

</script>
