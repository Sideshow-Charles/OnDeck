<template>
  <div class="main__container">
    <div class="main__text__container">
      <h1 class="main__text"> Ondeck is your remote <span>conference calling tool.</span></h1>
      <p class="sub__text"> Ondeck is a service that allows you to create beautiful, online, and encrypted <br> video calls for you and your remote team.</p>
      <AppButton style="margin-top: 15px; margin-bottom: 15px; padding-left: 40px; padding-right: 40px"></AppButton>
      <p class="final__text">5.0 Rating based on reviews from:</p>
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

.main__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  max-width: 106.5rem;
  padding-left: 128px;
  padding-right: 128px;
  padding-top: 6rem;
}

.main__text__container {
  line-height: 1.5;
  font-family: "Poppins", sans-serif;
}

.main__text {
  font-size: 55px;
  font-weight: bolder;
}

.main__text span {
  color: #e9ae17;
}

.sub__text {
  font-size: 16px;
  font-weight: 300;
  color: #706c6c;
  line-height: 1.9;
}

.final__text {
  font-size: 16px;
  font-weight: 300;
  color: #706c6c;
}

@media only screen and (max-width: 1200px) {
  .main__container {
    padding-left: 64px;
    padding-right: 64px;
  }
}

@media only screen and (max-width: 980px) {
  .main__container {
   display: block;
    padding-left: 24px;
    padding-right: 24px;
  }

  .main__text {
  font-size: 45px;
}

  .hero__image {
    display: none;
  }
}

@media only screen and (max-width: 576px) {
.main__text {
  font-size: 40px;
}

.sub__text {
  font-size: 16px;

}

.final__text {
  font-size: 16px;
}
}
</style>