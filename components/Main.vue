<template>
  <div class="hero__section">
    <!-- NavBar Section -->
    <nav class="nav__bar">
      <div class="company__logo">
        <img src="../assets/Logo.svg" alt="LOGO" />
      </div>

      <ul v-show="!mobile" class="nav__links__center">
        <NuxtLink to="#"><li @mouseover="showdropDown" @mouseleave="hidedropDown" class="nav__link__center">Products</li></NuxtLink>

        <div v-show= "dropDown" class="dropdown__menu">
          <div class="menu__item">
            <img src="../assets/Spense.svg" alt="Spense Logo">

            <div class="dropdown__menu__content">
            <p class="menu__header">Spense</p>
            <p class="menu__sub__text">Spense is a landing pade for writers. Great for practicing absolute positioning and flex layouts.</p>
            </div>

          </div>

          <div class="menu__item">
            <img src="../assets/Fiber.svg" alt="Spense Logo">

            <div class="dropdown__menu__content">
            <p class="menu__header">Fiber Landing Page</p>
            <p class="menu__sub__text">An online portfolio generator. Great to practice flex/grid layouts, and absolute positioning.</p>
            </div>

          </div>

          <div class="menu__item">
            <img src="../assets/Gradie.svg" alt="Spense Logo">

            <div class="dropdown__menu__content">
            <p class="menu__header">Gradie Sign Up Page</p>
            <p class="menu__sub__text">Gradie is a simple sign up page, great to practice centerinalavouts.</p>
            </div>

          </div>

        </div>

        <NuxtLink to="#"><li class="nav__link__center">Challenges</li></NuxtLink>
        <NuxtLink to="#"><li class="nav__link__center">Resources</li></NuxtLink>
        <NuxtLink to="#"><li class="nav__link__center">Other Links</li></NuxtLink>
      </ul>

      <ul v-show="!mobile" class="nav__links__right">
        <NuxtLink to="#"><li class="nav__link__right">Sign In</li></NuxtLink>
        <AppButton style="font-size: 14px"></AppButton>
      </ul>


      <img src="../assets/Menu.svg" alt="hamburger-menu" class="hamburger__menu" @click="toggleMobileNav" v-show="mobile">
      
      
    </nav>

    <!-- Mobile nav -->
    <div class="mobile__nav" v-show="mobileNav">
      <ul class="mobile__nav__links">
        <NuxtLink to="#"><li class="mobile__nav__link">Products</li></NuxtLink>
        <NuxtLink to="#"><li class="mobile__nav__link">Challenges</li></NuxtLink>
        <NuxtLink to="#"><li class="mobile__nav__link">Resources</li></NuxtLink>
        <NuxtLink to="#"><li class="mobile__nav__link">Other Links</li></NuxtLink>
      
        <NuxtLink to="#"><li class="mobile__nav__link">Sign In</li></NuxtLink>

        <AppButton style="font-size: 14px; padding-left: 40px; padding-right: 40px; padding-top: 12px; padding-bottom: 12px"></AppButton>

      </ul>
    </div>
    <!-- End of Mobile nav -->

    <!-- End  NavBar Section -->

    <Section></Section>

    <Brands></Brands>
  </div>
</template>

<script>
import Section from "./Section.vue";
import AppButton from "./UI/AppButton.vue";
import Brands from "./Brands.vue";
export default {
  components: {
    AppButton,
    Section,
    Brands,
  },
     data () {
       return {
          mobileNav: null,
          mobile: null,
          windowWidth: null,
          dropDown: false,
       }
     },

    mounted () {
       window.addEventListener("resize", this.checkScreen);
       this.checkScreen();
    },

     methods: {
       toggleMobileNav() {
         this.mobileNav = !this.mobileNav
       },
       
       showdropDown() {
         this.dropDown = !this.dropDown
       },

       hidedropDown() {
         if (this.dropDown = true) {
            this.dropDown = false;
         }
       },

       // Checks the screen size to show or hide the mobile nav. 

       checkScreen() {
         this.windowWidth = window.innerWidth;
         if (this.windowWidth <= 980) {
           this.mobile = true;
           return;
         } 
        this.mobile = false;
        this.mobileNav = false;
        return;
       },
     }

};
</script>

<style>
.hero__section {
  background-color: #f3ebe3;
  overflow: auto;
  height: 100vh;
}

.nav__bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  max-width: 106.5rem;
  padding-left: 128px;
  padding-right: 128px;
  padding-top: 2rem;
}

.nav__links__center {
  font-family: "Poppins", sans-serif;
  display: flex;
  justify-content: space-around;
  width: 40%;
}

.nav__link__center {
  list-style: none;
  font-size: 14px;
}

.nav__links__center a {
  text-decoration: none;
  color: #706c6c;
}

.nav__links__right {
  font-family: "Poppins", sans-serif;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 20%;
}

.nav__link__right {
  list-style: none;
  font-size: 14px;
}

.nav__links__right a {
  text-decoration: none;
  color: #706c6c;
}

.dropdown__menu {
  position: absolute;
  top: 10%;
  left: 20%;
  background: #fff;
  width: 30%;
  padding: 25px;
  border-radius: 10px;
}

.menu__item {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-left: 15px;
  margin-right: 15px;
  margin-bottom: 25px;
  margin-top: 25px;
}

.menu__item {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-left: 15px;
  margin-right: 15px;
  margin-bottom: 25px;
  margin-top: 25px;
}

.menu__item {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-left: 15px;
  margin-right: 15px;
  margin-bottom: 25px;
  margin-top: 25px;
}

.dropdown__menu__content {
  margin-left: 10px;
}

.menu__header {
  font-size: 14px;
  font-weight: bolder;
  margin-bottom: 5px;
}

.menu__sub__text {
  color: #706c6c;
  font-size: 12px;
  line-height: 1.8;
}

@media only screen and (max-width: 1200px) {
  .nav__bar {
     padding-left: 64px;
     padding-right: 64px;
  }
}

@media only screen and (max-width: 980px) {
  .nav__bar {
    padding-left: 24px;
    padding-right: 24px;
  }

  .nav__links__center {
    display: none;
  }

  .nav__links__right {
    display: none;
  }

  .nav__links__right {
    display: none;
  }

  .hamburger__menu {
    /* display: block; */
    height: 35px;
    width: 35px;
    cursor: pointer;
    margin-bottom: 5px;

  }
}

.mobile__nav {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #f3ebe3;
  padding-top: 20px;
  padding-bottom: 20px;
  height: 100vh;
  overflow: auto;
  /* z-index: 100; */
  position: absolute;
  width: 100%;
  margin-top: 30px;
}

.mobile__nav__link {
  padding: 25px 0;
  list-style: none;
  text-align: center;
  margin: 25px 0;
}

 a {
  text-decoration: none;
  color: #706c6c;
  font-family: "Poppins", sans-serif;
  font-size: 14px;
}
</style>