<template>
  <header>
    <div class="header__menu" :class="scrolled ? 'sticky' : ''">
      <div class="header__menu-wrapper container-xl">
        <Navbar />
      </div>
    </div>
    <div class="header__hero container-xl">
      <p>Hi, new friend!</p>
      <h1>We do not cook, we create your emotions!</h1>
      <p>
        Consectetur numquam poro nemo veniam eligendi rem adipisci quo modi.
      </p>
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
  data() {
    return {
      scrolled: false,
    };
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 0;
    },
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  unmounted() {
    window.removeEventListener("scroll", this.handleScroll);
  },
};
</script>

<style lang="scss">
.header__menu {
  display: flex;
  align-items: center;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 9999;
  border-bottom: solid 1px $lightGray;
  border-top: solid 1px $lightGray;
  background-color: rgba(255, 255, 255, 0.92);
  &-wrapper {
    display: flex;
    align-items: center;
  }
}

.header__hero {
  height: 300vh;
  margin-top: 16rem;
}

.sticky {
  box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.05);
}
</style>