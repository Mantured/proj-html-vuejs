<template>
  <section class="header-wrapper">
    <div class="header-top">
      <div class="row">
        <div class="col-3">
          <img
            src="../assets/images/Logo/avadabarbers-logo-x2-200x70.png"
            alt="logo avada barbers"
          />
        </div>
        <div class="col text-end align-self-center">
          <i class="fas fa-shopping-cart me-3"></i>
          <i class="fas fa-bars"></i>
        </div>
      </div>
    </div>
    <div class="header-bottom">
      <div class="row h-100">
        <div
          class="col d-flex flex-column justify-content-center align-items-start"
        >
          <h1>Barber Shop</h1>
          <!-- div interim -->
          <div class="separator"></div>
          <p>The Pinnacle of Male Grooming</p>
          <button class="my-btn-style">learn more</button>
        </div>
        <div class="col-6 h-100">
          <img
            class="img-fluid h-100"
            src="../assets/images/Header-Jumbo/avadabarbers_hero_focalmirror-800x1100.png"
            alt="barber cutting hair"
          />
        </div>
      </div>
      <i class="fab fa-opencart"></i>
      <i class="fab fa-wpressr"></i>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";
section.header-wrapper {
  height: 100vh;
  background-size: cover;
  background-position: center;
  background-image: url(../assets/images/Header-Jumbo/avadabarbers-homepage-hero-bg.jpg);
  div.header-top,
  div.header-bottom {
    width: 70vw;
    margin: 0 auto;
  }
  div.header-top {
    /* width: 70vw;
    margin: 0 auto; */
    /* position: fixed;
    left: 50%;
    transform: translate(-50%); */
    line-height: 120px;
    i {
      color: #ffffff;
      font-size: 1.5rem;
    }
  }
  div.header-bottom {
    /* width: 70vw;
    margin: 0 auto; */
    height: 85%;
    line-height: 85px;
    h1 {
      font-size: 5.5rem;
    }
    div.separator {
      border: 0.4px solid $Driftwood;
      width: 16rem;
    }
    p {
      font-size: 1.5rem;
      color: $Emperor;
    }
    i {
      position: fixed;
      right: 5px;
      z-index: 3;
      width: 60px;
      padding: 0.5rem;
      font-size: 2rem;
      text-align: center;
      color: $KashmirBlue;
      border-radius: 0.3rem;
      background-color: white;
      &.fab.fa-opencart {
        top: 180px;
      }
      &.fab.fa-wpressr {
        top: 235px;
      }
    }
  }
}
</style>
