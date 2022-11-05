<template>
  <div class="component">
    <form @submit.prevent="submitData">
      <input
        type="text"
        placeholder="Username"
        v-model="enteredUsername"
        required
      />
      <input
        type="number"
        placeholder="Age"
        v-model="enteredAge"
        min="4"
        max="150"
        required
      />
      <button>Update user</button>
    </form>
  </div>
</template>

<script>
export default {
  emits: ["update-user"],
  data() {
    return {
      enteredUsername: "",
      enteredAge: "",
    };
  },
  methods: {
    submitData() {
      this.$emit("update-user", this.enteredUsername, this.enteredAge);
    },
  },
};
</script>

<style>
form {
  width: 50vw;
  display: flex;
  justify-content: space-around;
}
</style>
