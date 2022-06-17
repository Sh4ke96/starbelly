<template>
  <div class="app">
    <Header />
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
:root {
  --primary: #f5c332;
  --secondary: #231e41;
  font-size: 10px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: var(--secondary);
  font-family: "Rubik", sans-serif;
}
</style>
