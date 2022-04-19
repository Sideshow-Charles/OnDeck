<template>
  <div class="brands__container">
    <div class="brands__header">
      <h2>Trusted by 3+ million people at companies like</h2>
    </div>
    <div class="brands__icons">
      <img
        src="../assets/NetflixLogo.svg"
        alt="Netflix Logo"
        class="netflix__logo"
      />
      <img
        src="../assets/ShopifyLogo.svg"
        alt="Shopify Logo"
        class="shopify__logo"
      />
      <img
        src="../assets/SpotifyLogo.svg"
        alt="Stopify Logo"
        class="spotify__logo"
      />
      <img
        src="../assets/WalmartLogo.svg"
        alt="Walmart Logo"
        class="walmart__logo"
      />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.brands__container {
  margin-top: 50px;
  padding: 24px 0;
  /* border: 3px solid pink; */
}

.brands__header h2 {
  font-family: "Poppins", sans-serif;
  text-align: center;
  font-size: 16px;
  color: #706c6c;
  
}

.brands__icons {
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 106.5rem;
  margin: 35px auto;
  padding: 0 15rem;
}

.brands__icons img {
  margin: 0 20px
}

@media only screen and (max-width: 980px) {
  .brands__icons {
    flex-wrap: wrap;
    margin: 20px 0;
    padding: 0;
  }

  .brands__icons img {
    margin: 20px;
  }
}

@media only screen and (max-width: 576px) {
  .brands__header h2 {
    padding: 0 12px;
    font-size: 14px;
  }

  .brands__icons {
    flex-wrap: wrap;
    margin: 30px 0;
    padding: 0;
  }

   .brands__icons img {
    width: 30%;
  }
}

/* @media only screen and (max-width: 414px) {
  .brands__header h2 {
    padding: 0 12px;
    font-size: 14px;
  }

  .brands__icons {
    flex-wrap: wrap;
    margin: 30px 0;
    padding: 0;
  }

   .brands__icons img {
    width: 35%;
  }
} */
</style>