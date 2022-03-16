<template>
  <div id="index-style" class=" h-screen w-scream text-center">
    <CardBody />

  </div>

</template>

<style>
#index-style {
  background-color: #ddd;
  height: 100vh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

</style>

<script>
import CardBody from '~/components/CardBody.vue'

export default {
  components: { CardBody },
  name: 'IndexPage'

}
</script>
