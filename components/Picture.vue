<template>
  <div>
    <!-- <img :src="avatar" :alt="descricao" :name="name"> --><!-- essa forma :src="avatar" é o mesmo que usar o v-bind:href="meu_link" -->
    <input :type="type" :name="name_input" />
  </div>
</template>

<script>
export default {
  name: 'Picture',
  data() {
    return {
      avatar: '/assets/img/eu.jpg',
      descricao: 'foto avatar',
      name: 'Gabriel',
      type: 'text',
      name_input: 'Gabriel'
    }
  }

}

</script>
