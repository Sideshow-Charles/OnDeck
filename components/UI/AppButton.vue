<template>
  <button
    class="app__button"
    
    v-bind="$attrs"
    v-on="$listeners"
  >
    <slot />Try for free
  </button>
</template>

<script>
export default {
  name: "AppButton",
  props: {
    btnStyle: {
      type: String,
      default: "",
    },
  },
};
</script>

<style>
.app__button {
  padding: 15px 25px;
  color: #fff;
  background-color: rgb(13, 73, 13);
  border: none;
  border-radius: 7px;
  cursor: pointer;
  font-size: 16px;
   font-family: "Poppins", sans-serif;
}

.app__button:hover {
  background-color: rgb(1, 97, 1);
}

@media only screen and (max-width: 576px) {
  .app__button {
    padding: 12px 10px;
    font-size: 14px;
  }
}
</style>