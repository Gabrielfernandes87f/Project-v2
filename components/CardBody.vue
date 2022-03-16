<template>
  <div id="card-body" class="text-center bg-teal-700 text-lg">

    <h1>titulo do card</h1>
    <p>tag do card</p>
    <p> description do card</p>

  </div>
</template>

<style>
#card-body {
  background-color: rgb(77, 8, 118);
  width: 350px;
  height: 350px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: -100px;
  border: solid 10px rgb(60, 6, 6);
  color : #fff;

}
</style>


<script>
export default {
  name: 'CardBody',

}
</script>
