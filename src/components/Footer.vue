<template>
  <section id="about-us">
    <div class="container">
      <div class="row">
        <div class="col-5 text-center">
          <img
            class="img-fluid"
            src="../assets/images/Footer-Credits/avadabarbers_footer_shop_image.png"
            alt=""
          />
          <button class="my-btn-style">shop our range now</button>
        </div>
        <div
          class="col d-flex justify-content-evenly align-items-center flex-column text-center"
        >
          <img
            src="../assets/images/Logo/avadabarbers-logo-x1.png"
            alt="Logo Avada Barbers"
          />
          <p>
            Avada Barbers <br />
            123 New York Street <br />
            New York City <br />
            info@yourwebsite.com <br />
            +1 (555) 555-1212 <br />
          </p>
          <div class="social-net">
            <button class="m-3">FOLLOW US</button>
            <div class="icons d-flex justify-content-evenly">
              <a href=""><i class="fab fa-facebook-f"></i></a>
              <a href=""><i class="fab fa-instagram"></i></a>
              <a href=""><i class="fab fa-twitter"></i></a>
              <a href=""><i class="fab fa-youtube"></i></a>
            </div>
          </div>
        </div>
        <div class="col-5 text-center">
          <img
            class="img-fluid"
            src="../assets/images/Footer-Credits/avadabarbers_footer_appointment_image.png"
            alt="image of barber meanwhile works"
          />
          <button class="my-btn-style">book your appointment</button>
        </div>
      </div>
    </div>
    <div class="rights-reserved">
      <p class="m-0">
        © Copyright 2012 - 2022 | Avada Theme by
        <a href="http://theme-fusion.com">ThemeFusion</a> | All Rights Reserved
        | Powered by <a href="http://wordpress.org">WordPress</a>
      </p>
    </div>
  </section>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Footer",
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/scss/style.scss";
section#about-us {
  /* height: 45vh; */
  background-color: $ColdGrey;
  button {
    scale: 0.7;
    margin-bottom: 2rem;
  }
}
div.row .col-5 {
  padding: 4rem;
  img {
    scale: 0.65;
  }
}
div.row .col {
  color: $Emperor;
  .social-net {
    button {
      background-color: transparent;
      border: none;
      color: $Driftwood;
      font-weight: 500;
    }
    .icons {
      a {
        text-decoration: none;
        color: $Emperor;
      }
    }
  }
}

div.rights-reserved {
  height: 10vh;
  background-color: #171717;
  /* text-align: center; */
  display: flex;
  align-items: center;
  justify-content: center;
  p {
    color: $Emperor;
    font-size: 0.8rem;
    a {
      text-decoration: none;
      color: $Driftwood;
    }
  }
}
/* .social-net {
  display: flex;
  justify-content: space-evenly;
} */
</style>
