<template>
  <section class="header-wrapper relative">
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
          <!-- <i class="fas fa-bars"></i> -->
          <div class="collapsible-menu">
            <input type="checkbox" id="menu" />
            <label for="menu"><i class="fas fa-bars"></i></label>
            <div class="menu-content">
              <ul>
                <li><a href="">Home</a></li>
                <li id="about-us-menu"><a href="#about-us">About Us</a></li>
                <li><a href="">Services</a></li>
                <li><a href="">Shop</a></li>
                <li><a href="">Our Team</a></li>
                <li><a href="">Blog</a></li>
                <li><a href="">Contact Us</a></li>
              </ul>
            </div>
          </div>
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
    top: 0;
    left: 50%; */
    line-height: 120px;
    /* transform: translateX(-50%); */
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
      width: 16rem;
      border: 0.4px solid $Driftwood;
    }
    p {
      color: $Emperor;
      font-size: 1.5rem;
    }
    i {
      right: 5px;
      width: 60px;
      z-index: 3;
      padding: 0.5rem;
      font-size: 2rem;
      position: fixed;
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

//? collapse menu plus
.collapsible-menu {
  background-color: transparent;
  display: inline;
}
.collapsible-menu ul {
  list-style-type: none;
  padding: 0;
}
.collapsible-menu li {
  display: flex;
  flex-direction: column;
  align-items: center;
  list-style-type: none;
  justify-content: center;
  a {
    text-decoration: none;
    color: $Ebb;
    font-size: 1.5rem;
  }
}
.collapsible-menu label {
  display: inline;
  cursor: pointer;
  /* padding: 10px 0 10px 50px; */
}
input#menu {
  display: none;
}
.menu-content {
  max-height: 0;
  overflow: hidden;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: $ColdGrey;
  filter: opacity(0.6);
  z-index: 3;
  line-height: 65px;
  display: flex;
  align-items: center;
  justify-content: center;
  /* transform: translateY(-50%); */
}
/* Toggle Effect */
input:checked ~ label {
  /*   background-image: url(../assets/images/Hover/times-solid.svg);
  color: #ffffff;
  display: block;
  position: absolute;
  top: 0;
  right: 10px;
  z-index: 3; */
  /* color: $Driftwood; */
}
input:checked ~ .menu-content {
  max-height: 100vh;
  max-width: 100vw;
}
/* #about-us-menu :hover.menu-content {
  background-image: url(../assets/images/Header-Jumbo/avadabarbers-homepage-hero-bg.jpg);
  background-size: cover;
} */
.collapsible-menu li:hover a {
  color: $Driftwood;
}
/* .collapsible-menu li#about-us-men:hover ~ .menu-content {
  background-image: url(../assets/images/Header-Jumbo/avadabarbers-homepage-hero-bg.jpg);
  background-size: cover;
  height: 100%;
  background-color: transparent;
} */
</style>
