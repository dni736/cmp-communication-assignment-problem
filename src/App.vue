<template>
  <div id="container">
    <user-data @update-user="updateUser"></user-data
    ><active-user :username="this.username" :age="this.age"></active-user>
  </div>
</template>

<script>
import ActiveUser from "./components/ActiveUser.vue";
import UserData from "./components/UserData.vue";

export default {
  components: { ActiveUser, UserData },
  data() {
    return {
      username: "",
      age: "",
    };
  },
  methods: {
    updateUser(username, age) {
      this.username = username;
      this.age = age;
    },
  },
};
</script>

<style>
#container {
  display: flex;
  align-items: baseline;
}
.component {
  width: 50vw;
  height: auto;
  display: flex;
  align-items: baseline;
  justify-content: space-around;
}
</style>
