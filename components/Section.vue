<template>
  <div class="section__container">
    <div class="section__text__container">
      <h1 class="section__text"> Ondeck is your remote <span>conference calling tool.</span></h1>
      <p class="section__sub__text"> Ondeck is a service that allows you to create beautiful, online, and encrypted <br> video calls for you and your remote team.</p>
      <AppButton style="margin-top: 15px; margin-bottom: 15px; padding-left: 40px; padding-right: 40px"></AppButton>
      <p class="section__final__text">5.0 Rating based on reviews from:</p>
    </div>
    <img src="../assets/Hero-Image.png" width="400px" height="auto" alt="Hero Image" class="hero__image" />
  </div>
</template>

<script>
import AppButton from "./UI/AppButton.vue";
export default {
  components: { AppButton }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap");

.section__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  max-width: 106.5rem;
  padding-left: 128px;
  padding-right: 128px;
  padding-top: 6rem;
}

.section__text__container {
  line-height: 1.5;
  font-family: "Poppins", sans-serif;
}

.section__text {
  font-size: 55px;
  font-weight: bolder;
}

.section__text span {
  color: #e9ae17;
}

.section__sub__text {
  font-size: 16px;
  font-weight: 300;
  color: #706c6c;
  line-height: 1.9;
}

.section__final__text {
  font-size: 16px;
  font-weight: 300;
  color: #706c6c;
}

@media only screen and (max-width: 1200px) {
  .section__container {
    padding-left: 64px;
    padding-right: 64px;
  }
}

@media only screen and (max-width: 980px) {
  .section__container {
   display: block;
    padding-left: 24px;
    padding-right: 24px;
  }

  .section__text {
  font-size: 45px;
}

  .hero__image {
    display: none;
  }
}

@media only screen and (max-width: 576px) {
.section__text {
  font-size: 40px;
}

.section__sub__text {
  font-size: 16px;

}

.section__final__text {
  font-size: 16px;
}
}
</style>