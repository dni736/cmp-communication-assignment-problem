<template>
  <div class="component">
    <h2>Username: {{ username }}</h2>
    <h3>Age: {{ age }}</h3>
  </div>
</template>

<script>
export default {
  props: ["username", "age"],
};
</script>

<style scoped>
.component {
  background-color: lightblue;
}
</style>
