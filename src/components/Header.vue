<template>
  <header>
    <div class="container-xl header__wrapper">
      <div class="header__logo">
        <a href="/" class="logo">
          <img src="../assets/img/logo.svg" alt="Starbelly" />
        </a>
      </div>
      <div class="header__menu">
        <Navbar />
      </div>
    </div>
  </header>
</template>

<script>
import Navbar from "./Navbar.vue";

export default {
  name: "Header",
  components: {
    Navbar,
  },
};
</script>

<style>

header {
  padding: 0 1.5rem;
  position: relative;
  height: 12rem;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: 0.3s ease-in-out;
}

.header__wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
}

.header__menu {
  display: flex;
  align-items: center;
}

</style>