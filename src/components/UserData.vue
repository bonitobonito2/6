<template>
  <div class="form">
    <input
      placeholder="user name"
      v-model="name"
      v-on:keyup.enter="changeNamee"
    />
    <input
      placeholder="user age"
      v-model="age"
      v-on:keyup.enter="changeNamee"
    />

    <button @click="changeNamee">save information</button>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      name: "",
      age: "",
    };
  },
  methods: {
    changeNamee() {
      this.$emit("change-name", [this.name, this.age]);
      this.name = "";
      this.age = "";
    },
  },
};
</script>

<style>
.form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.form input {
  width: 250px;
  background-color: rgb(215, 203, 203);
  border: none;
  height: 40px;
}
.form button {
  background-color: blue;
  border: none;
  height: 40px;
  color: white;
  font-size: 20px;
  cursor: pointer;
}
</style>
