<template>
  <div class="xd">
    <active-user :userName="userName" :age="age"> </active-user>
    <user-data :nameValue="userName" @changeName="changeName"></user-data>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userName: "",
      age: "",
    };
  },
  methods: {
    changeName: function (name) {
      this.userName = name[0];
      this.age = name[1];
    },
  },
};
</script>
<style>
.xd {
  display: flex;
  margin: 0 auto;
  gap: 200px;
}
</style>
