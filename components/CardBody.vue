<template>
  <div>
    <p>Gabriel fernandes</p>
    <p>Saudação: {{ message }}</p>
  </div>
</template>
<script>
export default {
  name: 'CardBody',
  data() {
    return {
      message: "Seja bem vindo ao vue"
    }
  }
}
</script>
