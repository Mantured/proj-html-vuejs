<template>
  <section class="jumbotron container-fluid">
    <div class="container">
      <div class="row centralize-paragraph">
        <div class="col-6 text-paragraph">
          <h5>award winning</h5>
          <h3>Pro Barbers</h3>
          <button class="btn my-btn-style">meet your new barber</button>
        </div>
      </div>
    </div>
    <svg
      class="fusion-big-triangle-candy"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="100"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
      style="fill: #ffffff; padding: 0"
    >
      <path d="M0 100 L50 2 L100 100 Z"></path>
    </svg>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Jumbotron",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";
section.jumbotron {
  height: 560px;
  background-size: cover;
  background-image: url(../assets/images/Header-Jumbo/avadabarbers-about-introbackground.jpg);
  /* can we used that for every phara? */
  div.container {
    height: 82.2%;
  }
}
</style>
