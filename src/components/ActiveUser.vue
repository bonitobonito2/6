<template>
  <div class="active">
    <h2 v-if="userName.length !== 0">name : {{ userName }}</h2>
    <h3 v-if="age.length !== 0">age : {{ age }}</h3>
  </div>
</template>

<script>
export default {
  props: {
    userName: {
      type: String,
      required: false,
    },
    age: {
      type: String,
      required: false,
    },
  },
};
</script>

<style>
.active {
  width: 200px;
}
</style>
