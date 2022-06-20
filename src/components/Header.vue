<template>
  <header>
    <div class="header__menu" :class="scrolled ? 'sticky' : ''">
      <div class="header__menu-wrapper container-xl">
        <Navbar />
      </div>
    </div>
    <div class="header__hero container-xl">
      <div class="row">
        <div class="col-lg-6">
          <div class="header__hero-main">
            <p class="header__aboveTitle">Hi, new friend!</p>
            <h1 class="header__title">
              We do not cook, we create your emotions!
            </h1>
            <p class="header__underTitle">
              Consectetur numquam poro nemo veniam eligendi rem adipisci quo
              modi.
            </p>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="header__hero-illustration">
            <img
              class="hero__food-1"
              src="../assets/img/illustration1.png"
              alt="food"
            />
            <img
              class="hero__food-2"
              src="../assets/img/illustration2.png"
              alt="food"
            />
            <img
              class="hero__food-3"
              src="../assets/img/illustration3.png"
              alt="food"
            />
            <div class="header__hero-dialog-1">
              <span>😋</span>
              Om-nom-nom...
            </div>
            <div class="header__hero-dialog-2">
              <span>🥰</span>
              Sooooo delicious!
            </div>
            <div class="header__hero-circle-1"></div>
            <div class="header__hero-circle-2"></div>
            <div class="header__hero-circle-3"></div>
            <div class="header__hero-circle-4"></div>
            <div class="header__hero-circle-5"></div>
            <img
              class="header__hero-icon-1"
              src="../assets/img/illustration1.svg"
              alt="phones"
            />
            <img
              class="header__hero-icon-2"
              src="../assets/img/illustration2.svg"
              alt="phones"
            />
            <img
              class="header__hero-icon-3"
              src="../assets/img/illustration3.svg"
              alt="phones"
            />
          </div>
        </div>
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
  margin-top: 25rem;
  &-main {
    .header__aboveTitle {
      display: inline-block;
      padding: 0.2rem 0.5rem;
      background-color: #f2f3f5;
      font-size: 1.2rem;
      font-weight: 400;
    }
    .header__underTitle {
      font-size: 1.6rem;
      color: $gray;
    }
  }
  &-illustration {
    position: relative;
    width: 100%;
    padding-bottom: 110%;
    .hero__food-1,
    .hero__food-2,
    .hero__food-3 {
      position: absolute;
      width: 45%;
    }
    .hero__food-1 {
      top: 9%;
      left: 5%;
      animation: animation-1 3s infinite ease-in-out;
    }
    .hero__food-2 {
      top: -11%;
      right: 16%;
      animation: animation-1 2s infinite ease-in-out;
    }
    .hero__food-3 {
      bottom: 33%;
      right: 14%;
      animation: animation-1 4s infinite ease-in-out;
    }
    .header__hero-dialog-1,
    .header__hero-dialog-2 {
      white-space: nowrap;
      opacity: 0;
      background-color: #ffffff;
      display: block;
      padding: 5px 30px 10px;
      position: absolute;
      font-weight: 500;
      font-size: 16px;
      letter-spacing: 0;
      border-radius: 20px;
      box-shadow: 0 2px 46px 0 rgba(0, 0, 0, 0.36);
    }
    .header__hero-dialog-1 {
      top: 0%;
      right: 35%;
      margin-right: -30px;
      animation: message 0.4s ease-in-out;
      animation-delay: 0s;
      animation-fill-mode: none;
      animation-fill-mode: forwards;
      animation-delay: 2s;
    }
    .header__hero-dialog-2 {
      bottom: 60%;
      left: 25%;
      margin-right: 30px;
      animation: message 0.4s ease-in-out;
      animation-delay: 0s;
      animation-fill-mode: none;
      animation-fill-mode: forwards;
      animation-delay: 1s;
    }
    .header__hero-dialog-1 span,
    .header__hero-dialog-2 span {
      display: inline-block;
      margin-right: 15px;
      font-size: 26px;
      transform: translateY(5px);
    }
    .header__hero-dialog-1::after,
    .header__hero-dialog-2::after {
      transform: rotate(45deg);
      content: "";
      position: absolute;
      z-index: 9;
      bottom: -5px;
      right: 30px;
      background-color: #ffffff;
      height: 10px;
      width: 10px;
    }
    .header__hero-circle-1 {
      position: absolute;
      height: 100px;
      width: 100px;
      border-radius: 50%;
      border: solid 22px #ffffff;
      right: 20%;
      top: 18%;
      box-shadow: inset 0 3px 6px 0 rgba(0, 0, 0, 0.09),
        0 3px 6px 0 rgba(0, 0, 0, 0.09);
      animation: animation-3 3s 1s infinite ease-in-out;
    }
    .header__hero-circle-2 {
      position: absolute;
      top: 13%;
      left: 20%;
      height: 25px;
      width: 25px;
      background-color: #f5c332;
      border-radius: 50%;
      box-shadow: 0 3px 6px 0 rgba(0, 0, 0, 0.09);
      animation: animation-1 2s 3s infinite ease-in-out;
    }
    .header__hero-circle-3 {
      position: absolute;
      bottom: 48%;
      right: 50%;
      width: 55px;
      height: 55px;
      background-color: #f5c332;
      border-radius: 50%;
      box-shadow: 0 3px 6px 0 rgba(0, 0, 0, 0.09);
      animation: animation-1 3s infinite ease-in-out;
    }
    .header__hero-circle-4 {
      position: absolute;
      bottom: 66%;
      right: 20%;
      width: 15px;
      height: 15px;
      background-color: #f5c332;
      border-radius: 50%;
      box-shadow: 0 3px 6px 0 rgba(0, 0, 0, 0.09);
      animation: animation-1 3s 4s infinite ease-in-out;
    }
    .header__hero-circle-5 {
      position: absolute;
      height: 40px;
      width: 40px;
      border-radius: 50%;
      border: solid 10px #ffffff;
      left: 20%;
      bottom: 52%;
      box-shadow: inset 0 3px 6px 0 rgba(0, 0, 0, 0.09),
        0 3px 6px 0 rgba(0, 0, 0, 0.09);
      animation: animation-3 3s 1.5s infinite ease-in-out;
    }
    .header__hero-icon-1,
    .header__hero-icon-2,
    .header__hero-icon-3 {
      position: absolute;
      width: 8%;
      opacity: 0.07;
    }
    .header__hero-icon-1 {
      top: -5%;
      left: 20%;
      animation: animation-2 3s 2s infinite ease-in-out;
    }
    .header__hero-icon-2 {
      right: 20%;
      bottom: 27%;
      animation: animation-2 3s 1s infinite ease-in-out;
    }
    .header__hero-icon-3 {
      left: 22%;
      bottom: 40%;
      animation: animation-2 3s infinite ease-in-out;
    }
  }
}

.sticky {
  box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.05);
}
</style>