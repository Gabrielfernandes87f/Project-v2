<!-- Please remove this file from your project -->
<template>
  <div class="text-center justify-center text-base max-h-fit pt-20">
    <h1>Olá Vue</h1>
    <div>
      {{ desc }}
    </div>
    <div class>
      <CardBody :mostrar_email="true" />
    <div>
     <InputType />
    </div>
    <div>
      <Pessoa />
    </div>
    <div>
      <Form
      emailProps="test@props"
      :inputColor="inputColor"
      :input-type="inputType"
      :inputName="inputName"
      />
    </div>
    </div>
  </div>
</template>

<script>
import CardBody from './CardBody'
import InputType from './InputType'
import Pessoa from './Pessoa'
import Form from './Form.vue'
export default {
  name: 'NuxtTutorial',
  components: {
    CardBody,
    InputType,
    Pessoa,
    Form
},
  data() {
    return {
      desc: 'Vue.js é uma biblioteca JavaScript de código aberto, desenvolvida pelo Vue.js Team, que permite a criação de interfaces de usuário através de componentes reutilizáveis.',
      inputColor: '#000',
      inputType: 'text',
      inputName: 'Nome'
    }
  }
}

</script>
